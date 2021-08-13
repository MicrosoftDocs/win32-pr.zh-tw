---
description: 包含在64位電腦上向系統註冊32位元件的同進程伺服器清單。 它包含每個元件的物件。
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: WOWInprocServers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: d85abf322d34d03c0f5e8863b5434343946b676e477e18077c82d83de78cafb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545569"
---
# <a name="wowinprocservers-collection"></a>WOWInprocServers 集合

包含在64位電腦上向系統註冊32位元件的同進程伺服器清單。 它包含每個元件的物件。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，但不支援 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法。 若要安裝或匯入元件到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。

## <a name="members"></a>成員

**WOWInprocServers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**Root**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [Clsid](#clsid)
-   [InprocServer32](#inprocserver32)
-   [ProgID](#progid)

### <a name="clsid"></a>CLSID



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 元件的 GUID。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                  |
| 類型           | String                                                                                                                                                    |
| 預設值        | N/A                                                                                                                                                       |
| 最小系統 | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| 進入 | 值 |
|----------------|----------------------------------|
| 描述    | 元件的檔案路徑。 |
| Access         | ReadOnly                         |
| 類型           | String                           |
| 預設值        | N/A                              |
| 最小系統 | Windows XP                       |



 

### <a name="progid"></a>ProgID



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 識別元件的名稱。 在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                            |
| 類型           | String                                                                                                                                                              |
| 預設值        | N/A                                                                                                                                                                 |
| 最小系統 | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
