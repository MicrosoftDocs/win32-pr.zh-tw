---
description: 包含 DCOM 要使用的通訊協定清單。 它包含每個通訊協定的物件。
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: DCOMProtocols 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: f387c9ba1d46b99c44a3d6616df95f7b6f9cece959a943b63ed12ce6fe8af900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548017"
---
# <a name="dcomprotocols-collection"></a>DCOMProtocols 集合

包含 DCOM 要使用的通訊協定清單。 它包含每個通訊協定的物件。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**DCOMProtocols** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**Root**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [名稱](#name)
-   [順序](#order)
-   [ProtocolCode](#protocolcode)

### <a name="name"></a>名稱



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 通訊協定的名稱。 在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | 讀寫                                                                                                                                                   |
| 類型           | String                                                                                                                                                      |
| 預設值        | 「新的通訊協定」                                                                                                                                              |
| 最小系統 | Windows 2000                                                                                                                                                |



 

### <a name="order"></a>單



| 進入 | 值 |
|----------------|-----------------------------------------|
| 描述    | 嘗試通訊協定的順序。 |
| Access         | 讀寫                               |
| 類型           | Long (0-65000)                           |
| 預設        | 0                                       |
| 最小系統 | Windows 2000                            |



 

### <a name="protocolcode"></a>ProtocolCode



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指定 RPC 通訊協定序列的程式碼。 支援的通訊協定代碼包含下列各項： ncacn \_ ip \_ tcp、ncacn \_ HTTP、ncacn \_ spx。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                                                                                                                                   |
| 類型           | String                                                                                                                                                                                                                                                                      |
| 預設值        | ""                                                                                                                                                                                                                                                                          |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
