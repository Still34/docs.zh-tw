---
title: COR_FIELD_OFFSET 結構
ms.date: 03/30/2017
api_name:
- COR_FIELD_OFFSET
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_FIELD_OFFSET
helpviewer_keywords:
- COR_FIELD_OFFSET structure [.NET Framework metadata]
ms.assetid: cced5298-277f-4a5a-8ecf-a0050c1096ea
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8c4a5c8efc87940b7df0bfd532beaa67931a8c81
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33442114"
---
# <a name="corfieldoffset-structure"></a>COR_FIELD_OFFSET 結構
儲存指定欄位的位移 (在類別中)。  
  
## <a name="syntax"></a>語法  
  
```  
typedef struct COR_FIELD_OFFSET {  
    mdFieldDef  ridOfField;  
    ULONG       ulOffset;  
} COR_FIELD_OFFSET;  
```  
  
## <a name="members"></a>成員  
  
|成員|描述|  
|------------|-----------------|  
|`ridOfField`|`mdFieldDef`中繼資料語彙基元所代表的欄位。|  
|`ulOffset`|欄位的位移在其類別中。|  
  
## <a name="remarks"></a>備註  
 [Imetadataimport:: Getclasslayout](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-getclasslayout-method.md)和[imetadataemit:: Setclasslayout](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setclasslayout-method.md)方法會採用一個參數類型`COR_FIELD_OFFSET`。  
  
## <a name="requirements"></a>需求  
 **平台：** 看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** CorHdr.h、 CorProf.idl  
  
 **.NET framework 版本：** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱  
 [中繼資料結構](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)  
 [IMetaDataEmit 介面](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataImport 介面](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
