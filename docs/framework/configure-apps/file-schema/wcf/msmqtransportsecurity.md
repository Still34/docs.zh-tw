---
title: '&lt;msmqTransportSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 092e911b-ab1b-4069-a26e-6134c3299e06
ms.openlocfilehash: f178ac3132e3c5880daef1d59480edae88f1d27e
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2018
ms.locfileid: "50180974"
---
# <a name="ltmsmqtransportsecuritygt"></a>&lt;msmqTransportSecurity&gt;
指定自訂繫結的 MSMQ 傳輸安全性設定。  
  
 \<system.serviceModel>  
\<繫結 >  
\<customBinding>  
\<繫結 >  
\<msmqIntegration >  
\<msmqTransportSecurity >  
  
## <a name="syntax"></a>語法  
  
```xml  
<msmqTransportSecurity>  
   msmqAuthenticationMode="None/Windows/Certificate"  
   msmqEncryptionAlgorithm="RC4Stream/AES"  
   msmqProtectionLevel="None/Sign/EncryptAndSign"  
   msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />  
</msmqTransportSecurity>  
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|`msmqAuthenticationMode`|指定 MSMQ 傳輸必須如何驗證訊息。 如果這設定為 `None`，則 `msmqProtectionLevel` 屬性的值也必須設定為 `None`。<br /><br /> 有效值包括以下的值：<br /><br /> -None： 沒有驗證。<br />-Windows： 驗證機制使用 Active Directory 與訊息相關聯的 SID 取得 X.509 憑證。 接著這會用於檢查佇列的 ACL，以確保使用者具有寫入佇列的權限。<br />-Certificate： 通道在從憑證存放區取得的憑證。<br /><br /> 預設值為 Windows。 此屬性的型別為 <xref:System.ServiceModel.MsmqAuthenticationMode>。|  
|`msmqEncryptionAlgorithm`|指定演算法，該演算法用於在訊息佇列管理員之間傳輸訊息時，在線上加密訊息。 有效值包括以下的值：<br /><br /> -RC4Stream<br />AES<br /><br /> 預設值為 RC4Stream。 此屬性的型別為 <xref:System.ServiceModel.MsmqEncryptionAlgorithm>。|  
|`msmqProtectionLevel`|指定在 MSMQ 傳輸層級上保護訊息的方式。 加密可確保訊息完整性，而 EncryptAndSign 可確保訊息完整性和不可否認性，也就是訊息確實來自寄件者，且寄件者就是他本人。 有效值包括以下的值：<br /><br /> -None： 無保護。<br />簽署： 簽署訊息。<br />-EncryptAndSign： 訊息會經過加密及簽署。<br /><br /> 預設值為 Sign。 此屬性的型別為 <xref:System.Net.Security.ProtectionLevel>。|  
|`msmqSecureHashAlgorithm`|指定計算摘要做為部分簽章時使用的演算法。 有效值包括以下的值：<br /><br /> -   MD5<br />-   SHA1<br />-   SHA256<br />-   SHA512<br /><br /> 預設值為 SHA1。 此屬性的型別為 <xref:System.ServiceModel.MsmqSecureHashAlgorithm>。|  
  
### <a name="child-elements"></a>子元素  
 無。  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[\<msmqIntegration >](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqintegration.md)|指定與 Message Queuing (MSMQ) 寄件者或收件者互動所需的設定。|  
|[\<msmqTransport >](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqtransport.md)|指定 Windows Communication Foundation (WCF) 服務的佇列通訊屬性 (該服務會使用原生 MSMQ 通訊協定)。|  
  
## <a name="remarks"></a>備註  
 如需有關傳輸安全性的詳細資訊，請參閱[傳輸安全性](../../../../../docs/framework/wcf/feature-details/transport-security.md)。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity>  
 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [WCF 中的佇列](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)  
 [傳輸](../../../../../docs/framework/wcf/feature-details/transports.md)  
 [選擇傳輸](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)  
 [繫結](../../../../../docs/framework/wcf/bindings.md)  
 [擴充繫結](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [自訂繫結](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [傳輸安全性](../../../../../docs/framework/wcf/feature-details/transport-security.md)
