---
title: 基本和摘要式驗證
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- authentication [.NET Framework], classes
- Basic authentication
- authentication [.NET Framework], basic
- client authentication, basic
- user authentication, basic
- authentication [.NET Framework], digest
- receiving data, authentication
- client authentication, digest
- Internet, authentication
- digest authentication
- sending data, authentication
- network resources, authentication
- user authentication, digest
ms.assetid: 8cce2742-8d52-4643-9dd2-64ddf38aa878
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 66b20c299252ff1f218a8131758e2cf03640aac6
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2018
ms.locfileid: "47199532"
---
# <a name="basic-and-digest-authentication"></a>基本和摘要式驗證
基本和摘要式驗證的 <xref:System.Net> 實作符合 RFC2617 - HTTP 驗證：基本和摘要式驗證 (可在全球資訊網協會的網站 www.w3.org 上取得)。  
  
 若要使用基本和摘要式驗證，應用程式必須在 <xref:System.Net.WebRequest> 物件的 <xref:System.Net.WebRequest.Credentials%2A> 屬性中提供使用者名稱和密碼，以用來從網際網路要求資料，如下列範例所示。  
  
```vb  
Dim MyURI As String = "http://www.contoso.com/"  
Dim WReq As WebRequest = WebRequest.Create(MyURI)  
WReq.Credentials = New NetworkCredential(UserName, SecurelyStoredPassword)  
```  
  
```csharp  
String MyURI = "http://www.contoso.com/";  
WebRequest WReq = WebRequest.Create(MyURI);  
WReq.Credentials = new NetworkCredential(UserName, SecurelyStoredPassword);  
```  
  
> [!CAUTION]
>  使用基本與摘要式驗證傳送的資料不會經過加密，因此敵人可以看到資料。 此外，基本驗證認證 (使用者名稱和密碼) 會以純文字傳送，而且可以被攔截。  
  
## <a name="see-also"></a>請參閱  
 [NTLM 與 Kerberos 驗證](../../../docs/framework/network-programming/ntlm-and-kerberos-authentication.md)  
 [網際網路驗證](../../../docs/framework/network-programming/internet-authentication.md)
