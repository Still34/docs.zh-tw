---
title: WCF 的 &lt;faultPropagationQuery&gt;
ms.date: 03/30/2017
ms.assetid: fabafbc8-3e45-4feb-8321-0725e9f4079c
ms.openlocfilehash: c3853c470a9243835e071d35008dfff5b885591d
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123315"
---
# <a name="ltfaultpropagationquerygt-of-wcf"></a>WCF 的 &lt;faultPropagationQuery&gt;

表示用來追蹤活動中發生之錯誤處理的查詢。  每當 FaultHandler 處理錯誤時，都會發生這個事件。 您應該使用這種查詢來追蹤活動中發生的錯誤處理。 追蹤參與者必須要具備查詢，才能訂閱錯誤傳播記錄。  
  
如需有關追蹤設定檔查詢的詳細資訊，請參閱 <<c0> [ 追蹤設定檔](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)。  
  
\<system.serviceModel>  
\<追蹤 >  
\<設定檔 >  
\<trackingProfile>  
\<工作流程 >  
\<faultPropagationQueries >  
\<faultPropagationQuery >  
  
## <a name="syntax"></a>語法  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String"/>
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```
  
## <a name="attributes-and-elements"></a>屬性和元素

下列章節說明屬性、子元素和父元素。

### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|`faultSourceActivityName`|字串，可指定傳用錯誤之錯誤處理常式活動的名稱。 預設值是\*，這表示所有活動傳回錯誤傳播記錄。|  
|`faultHandlerActivityName`|字串，可指定本身是錯誤來源的活動名稱。|  
  
### <a name="child-elements"></a>子元素

無。
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<faultPropagationQueries>](faultpropagationqueries-of-wcf.md)|代表組態項目的清單，可用來追蹤活動內發生之錯誤的處理。  每當 FaultHandler 處理錯誤時，都會發生這個事件。|
  
## <a name="see-also"></a>另請參閱  
 
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [工作流程追蹤及追蹤](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [追蹤設定檔](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
