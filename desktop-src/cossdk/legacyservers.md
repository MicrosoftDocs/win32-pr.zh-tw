---
description: 與 InprocServers 集合相同，不同之處在于此集合也包含本機伺服器。
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: LegacyServers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2ea542fa539ea1eb1cceae0f4cb8ba8dc2012085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991629"
---
# <a name="legacyservers-collection"></a>LegacyServers 集合

與 [**InprocServers**](inprocservers.md) 集合相同，不同之處在于此集合也包含本機伺服器。

此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**LegacyServers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**根**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [ClassName](#classname)
-   [Clsid](#clsid)
-   [InprocServer32](#inprocserver32)
-   [LocalServer32](#localserver32)
-   [ProgID](#progid)

### <a name="classname"></a>ClassName



| 進入 | 值 |
|----------------|------------------------|
| 描述    | 類別的名稱。 |
| Access         | ReadOnly               |
| 類型           | String                 |
| 預設值        | N/A                    |
| 最小系統 | Windows XP             |



 

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



 

### <a name="localserver32"></a>LocalServer32



| 進入 | 值 |
|----------------|---------------------------------------------------------------|
| 描述    | 指定32位本機伺服器應用程式的完整路徑。 |
| Access         | ReadOnly                                                      |
| 類型           | String                                                        |
| 預設值        | N/A                                                           |
| 最小系統 | Windows XP                                                    |



 

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

 

 
