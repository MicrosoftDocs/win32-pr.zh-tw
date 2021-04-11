---
description: 集合是標準的自動化概念，可提供一組物件的統一介面，讓您可以執行反復專案。
ms.assetid: c1ebe529-33cb-4158-923d-124d6328fc60
ms.tgt_platform: multiple
title: 存取 WMI 集合
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b875f50c1778a03c304f90c019da172be6ef5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194714"
---
# <a name="accessing-a-wmi-collection"></a>存取 WMI 集合

集合是標準的自動化概念，可提供一組物件的統一介面，讓您可以執行反復專案。 適用于 WMI 的腳本 API 會公開一些符合集合範例的介面。 在每個案例中，使用 **Item** 方法來識別使用包含值之字串的元素。

[**內含**](swbempropertyset.md)、 [**SWbemQualifierSet**](swbemqualifierset.md)和 [**SWbemMethodSet**](swbemmethodset.md)集合大多用來修改架構。 [**Swbemobjectset 搭配使用**](swbemobjectset.md)物件包含透過呼叫（例如 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)或 [**\_ SWBEMOBJECT. associators of**](swbemobject-associators-.md)）取得的 WMI 物件，例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)實例。 [**SWbemRefresher**](swbemrefresher.md)物件只能包含 WMI 類別的實例。 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件可能包含 WMI 物件或提供者針對方法呼叫所需的任何其他類型的資料。

> [!Note]  
> 下列主題主要是針對 VBScript 撰寫的。 C # 使用標準 [IEnumerable](/dotnet/api/system.collections.ienumerable) 介面來 collate 和列舉物件。 相反地，每當傳回值包含一個以上的結果時，PowerShell 通常會使用隱含的物件集合。

 

下表列出適用于 WMI 的腳本 API 中的集合，以及每個集合的元素和參數。



| 集合                                       | 元素                                              | Item () 參數                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**Swbemobjectset 搭配使用**](swbemobjectset.md)         | [**SWbemObject**](swbemobject.md)                   | 物件路徑                                                              |
| [**內含**](swbempropertyset.md)     | [**Swbempropertyset**](swbemproperty.md)               | 屬性名稱                                                            |
| [**SWbemQualifierSet**](swbemqualifierset.md)   | [**SWbemQualifier**](swbemqualifier.md)             | 限定詞名稱                                                           |
| [**SWbemMethodSet**](swbemmethodset.md)         | [**SWbemMethod**](swbemmethod.md)                   | 方法名稱                                                              |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | [**SWbemNamedValue**](swbemnamedvalue.md)           | 值名稱                                                               |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)   | [**SWbemPrivilege**](swbemprivilege.md)             | 許可權名稱                                                           |
| [**SWbemRefresher**](swbemrefresher.md)         | [**SWbemRefreshableItem**](swbemrefreshableitem.md) | [**SWbemRefresher**](swbemrefresher.md)物件中專案的索引 |



 

如需有關在集合中加入和移除專案的詳細資訊和範例，請參閱從集合 [移除單一專案](removing-a-single-item-from-a-collection.md) ，以及 [從集合中移除多個專案](removing-multiple-items-from-a-collection.md)。 如需使用類別的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

 

 
