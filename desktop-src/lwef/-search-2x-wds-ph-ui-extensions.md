---
title: 使用 Shell 擴充功能新增圖示和內容功能表
description: 您可以藉由執行 Shell 擴充功能，來改善使用者使用 Microsoft Windows 桌面搜尋 (WDS) 和通訊協定處理常式的體驗。
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "104185493"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a>使用 Shell 擴充功能新增圖示和內容功能表

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

您可以藉由執行 Shell 擴充功能，來改善使用者使用 Microsoft Windows 桌面搜尋 (WDS) 和通訊協定處理常式的體驗。 如果沒有進一步的擴充功能，您所建立的通訊協定處理常式將不會包含下列使用者體驗：

-   WDS 不會顯示結果的特定圖示。
-   當使用者按兩下專案時，使用者介面將不會回應事件。
-   當使用者以滑鼠右鍵按一下專案時，內容功能表將不支援此專案的任何作業。

**IShellFolder** 需要最基本的 **IPersist** 和 **IPersistFolder** ，而且 **ICoNtextMenu** 和 **IExtractIcon** 需要最基本的 **IShellFolder** 執行，這兩個介面可提供更順暢的使用者體驗。

 

## <a name="ipersist"></a>IPersist

**IPersist** 介面會定義單一方法 **GetClassID**，其設計目的是要提供可持續儲存在系統中之物件的 CLSID。



| 方法       | 描述                                 |
|--------------|---------------------------------------------|
| GetClassID ()  | 傳回通訊協定處理常式的 ClassID |



 

> [!Note]
>
> 應針對 **IPersist**、 **IPersistFolder** 和 **IShellFolder** 執行相同的 CLSID。

 

 

## <a name="ipersistfolder"></a>IPersistFolder

**IPersistFolder** 介面是用來初始化 Shell 資料夾物件。 此介面的實作為衍生自 **IPersist** 的介面，是資料夾在 Shell 命名空間中的通知位置。



| 方法       | 描述                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| 初始化 ()  | 指示 Shell 資料夾物件根據傳遞的資訊進行初始化，並傳回 S \_ 確定 |



 

> [!Note]
>
> 應針對 **IPersist**、 **IPersistFolder** 和 **IShellFolder** 執行相同的 CLSID。

 

您不會直接使用此介面。 它會在初始化 Shell 資料夾物件時，由 IShellFolder：： BindToObject 介面的檔案系統實作為使用。

 

## <a name="ishellfolder"></a>IShellFolder

**IShellFolder** 介面是用來管理資料夾，而且需要部分執行，如此一來，為通訊協定處理常式所執行的圖示和內容介面，在 Windows 桌面搜尋結果使用者介面中的行為就會正確。 需要的大部分功能都是透過 **GetUIObjectOf** 方法來公開。 這個方法可讓增益集查詢 **IExtractIcon** 和 **ICoNtextMenu** 介面。

**IShellFolder** 介面會使用 pidl 而非 url。 相較于完整命名空間延伸模組的需求，增益集可以使用僅包含 URL 的簡單 IDL 結構。

您必須執行下列 **IShellFolder** 方法。 請注意，其中五種方法需要進行基本的執行。



| 方法             | 描述                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject ()      | 傳回 E \_ >notimpl                                                                                                                                                                                          |
| BindToStorage ()     | 傳回 E \_ >notimpl                                                                                                                                                                                          |
| CreateViewObject ()  | 傳回 E \_ >notimpl                                                                                                                                                                                          |
| SetNameOf ()         | 傳回 E \_ >notimpl                                                                                                                                                                                          |
| ParseDisplayName ()  | 將 URL 轉換成 PIDL 結構                                                                                                                                                                        |
| CompareIDs ()        | 比較兩個 PIDL 值                                                                                                                                                                                    |
| GetDisplayNameOf ()  | 傳回 PIDL 的 URL。                                                                                                                                                                                  |
| GetUIObjectOf ()     | 這個方法類似于 OLE COM QueryInterface 方法。 如果要求的是圖示，呼叫端會要求 IID \_ IExtractIcon; 如果要求內容功能表，呼叫端會要求 iid \_ ICoNtextMenu。 |



 

> [!Note]
>
> 應針對 **IPersist**、 **IPersistFolder** 和 **IShellFolder** 執行相同的 CLSID。

 

**IShellFolder** 不會用來列舉資料夾。 這表示資料夾的顯示名稱將會是實體 URL。 未來可能會變更。

 

## <a name="icontextmenu"></a>ICoNtextMenu

當 WDS 向使用者顯示結果時，使用者可以在專案上按一下滑鼠右鍵，並查看 **ICoNtextMenu** 介面所定義的內容功能表。

操作功能表上的預設動作，與按兩下專案時所採取的動作相同。 如果專案沒有對應的 **IShellFolder** 或 **ICoNtextMenu** 介面，則按兩下事件的預設行為是將 URL 當作引數傳遞至 ShellExecute 函式。

 

## <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** 會根據您的通訊協定處理常式所提供的 PIDL URL，抓取 WDS 使用者介面的圖示。

 

## <a name="code-sample"></a>程式碼範例

[自訂通訊協定處理常式消費者介面範例程式碼](-search-2x-wds-ph-ui-samplecode.md)示範 **IShellFolder** 和支援介面的執行，並包含操作 pidl 的支援。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[自訂通訊協定處理常式消費者介面範例程式碼](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[安裝和註冊通訊協定處理常式](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




