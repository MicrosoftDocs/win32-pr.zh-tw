---
description: 抓取有關處理多個物件之方法的延伸錯誤資訊，例如在 COMAdminCatalogCollection 物件上填入和 SaveChanges，以及在 COMAdminCatalog 物件上安裝、匯入或匯出應用程式或元件的方法。
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: ErrorInfo 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9953bc1119d7e203936ca7e78048a4083a996ec2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881042"
---
# <a name="errorinfo-collection"></a>ErrorInfo 集合

抓取有關處理多個物件之方法的延伸錯誤資訊，例如在 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)和 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) ，以及在 [**COMAdminCatalog**](comadmincatalog.md)物件上安裝、匯入或匯出應用程式或元件的方法。

在 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)上使用 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)方法，以存取與原創組合（具有錯誤）相關聯的 **ErrorInfo** 集合。

一旦發生錯誤，您就必須立即在 **ErrorInfo** 上呼叫 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) ;否則會遺失錯誤資訊。

此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**ErrorInfo** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

除了 **ErrorInfo**、 [**InprocServers**](inprocservers.md)、 [**PropertyInfo**](propertyinfo.md)、 [**RelatedCollectionInfo**](relatedcollectioninfo.md)、 [**Root**](root.md)和 [**WOWInprocServers**](wowinprocservers.md)之外，您可以從每個集合流覽至這個集合。

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [ErrorCode](#errorcode)
-   [MajorRef](#majorref)
-   [MinorRef](#minorref)
-   名稱

### <a name="errorcode"></a>ErrorCode



| 進入 | 值 |
|----------------|----------------------------------------|
| 說明    | 物件或檔案的錯誤碼。 |
| Access         | ReadOnly                               |
| 類型           | String                                 |
| 預設        | None                                   |
| 最小系統 | Windows 2000                           |



 

### <a name="majorref"></a>MajorRef



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 說明    | 發生錯誤之物件的索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性值。 例如，如果集合中的特定物件上的 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 呼叫失敗，則會將該物件的索引 **鍵** 屬性值報告為 MajorRef 值。 您可以使用這個屬性來查看無法更新的專案，或找出無法安裝的元件或 DLL。 |
| Access         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 類型           | String                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 預設        | None                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 說明    | 具有錯誤之專案的精確規格，例如屬性名稱。 如果發生多個錯誤，或在不適用的內容中，MinorRef &lt; 無效 &gt; 。 |
| Access         | ReadOnly                                                                                                                                                                          |
| 類型           | String                                                                                                                                                                            |
| 預設        | None                                                                                                                                                                              |
| 最小系統 | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Name



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 說明    | 有錯誤的物件或檔案名。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                                                                                 |
| 類型           | String                                                                                                                                                                                                                   |
| 預設        | None                                                                                                                                                                                                                     |
| 最小系統 | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
