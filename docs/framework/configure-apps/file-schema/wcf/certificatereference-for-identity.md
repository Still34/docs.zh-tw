---
title: '&lt;身分識別&gt;的 &lt;certificateReference&gt;'
ms.date: 03/30/2017
ms.assetid: ac359c65-c22d-42d2-97de-db53b77cebdb
ms.openlocfilehash: 7c2ac27d547cdea959cca2ca4a0ffc9c9282c20d
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/03/2018
---
# <a name="ltcertificatereferencegt-for-ltidentitygt"></a>&lt;身分識別&gt;的 &lt;certificateReference&gt;
指定 X.509 憑證驗證的設定。 連接至使用這個身分識別端點的安全 Windows Communication Foundation (WCF) 用戶端會確認伺服器所呈現的宣告包含用來建構這個身分識別的身分識別宣告。  
  
 \<身分識別 >  
\<certificateReference >  
  
## <a name="syntax"></a>語法  
  
```xml  
<certificateReference   
        findValue="String"   
    isChainIncluded="Boolean"  
    storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"storeName="  
  
    storeLocation="LocalMachine/CurrentUser"  
  
X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier"  
</certificateReference>  
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|findValue|指定要在 X.509 憑證存放區中搜尋的值。 這個屬性所包含的型別必須滿足指定之 `X509FindType` 值的需求。 預設為空字串。|  
|isChainIncluded|布林值，這個值會指定是否使用憑證鏈結完成驗證。|  
|storeLocation|指定用戶端可用來驗證伺服器憑證之憑證存放區的位置。<br /><br /> 有效值包括以下的值：<br /><br /> -LocalMachine: 指派憑證存放區至本機電腦。<br />-CurrentUser: 指派憑證存放區目前的使用者。<br /><br /> 預設值為 LocalMachine。<br /><br /> 此屬性的型別為 <xref:System.Security.Cryptography.X509Certificates.StoreLocation>。|  
|storeName|指定要開啟之 X.509 憑證存放區的名稱。<br /><br /> 有效值包括以下的值：<br /><br /> -AddressBook： 其他使用者的憑證存放區。<br />-AuthRoot： 協力廠商憑證授權單位 (Ca) 的存放區的憑證。<br />-CertificateAuthority： 中繼 Ca 的憑證存放區。<br />-不允許： 憑證已撤銷之憑證存放區。<br />-My： 憑證個人憑證存放區。<br />-Root： 信任根 Ca 的憑證存放區。<br />-TrustedPeople： 直接信任之人員和資源的憑證存放區。<br />-TrustedPublisher： 直接信任之發行者的憑證存放區。<br /><br /> 預設值為 My。<br /><br /> 此屬性的型別為 <xref:System.Security.Cryptography.X509Certificates.StoreName>。|  
|X509FindType|指定要執行之 X.509 搜尋的型別。 `findValue` 屬性所包含的型別必須滿足指定之 X509FindType 的需求。<br /><br /> 有效值包括以下的值：<br /><br /> -FindByThumbPrint<br />-   FindBySubjectName<br />-FindBySubjectDistinguishedName<br />-FindByIssuerName<br />-FindByIssuerDistinguishedName<br />-FindBySerialNumber<br />-   FindByTimeValid<br />-   FindByTimeNotYetValid<br />-FindByTemplateName<br />-   FindByApplicationPolicy<br />-   FindByCertificatePolicy<br />-FindByExtension<br />-FindByKeyUsage<br />-   FindBySubjectKeyIdentifier<br /><br /> 預設值為 FindBySubjectDistinguishedName。<br /><br /> 此屬性的型別為 <xref:System.Security.Cryptography.X509Certificates.X509FindType>。|  
  
### <a name="child-elements"></a>子項目  
 無。  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[\<身分識別 >](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|指定設定，這個設定可讓其他端點與此端點交換訊息時啟用端點驗證。|  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.ServiceModel.Configuration.CertificateReferenceElement>  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>
