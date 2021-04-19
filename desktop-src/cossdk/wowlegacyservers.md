---
description: WOWLegacyServers 集合的公開屬性主要是與 LegacyServers 集合相同，不同之處在于 WOWLegacyServers 集合是從64位電腦上的32位登錄中繪製。
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: WOWLegacyServers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973571"
---
# <a name="wowlegacyservers-collection"></a>WOWLegacyServers 集合

**WOWLegacyServers** 集合的公開屬性主要是與 [**LegacyServers**](legacyservers.md)集合相同，不同之處在于 **WOWLegacyServers** 集合是從64位電腦上的32位登錄中繪製。

此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**WOWLegacyServers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

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

 

 
