---
description: 當您在 Windows Shell 中執行自訂檔案格式時，請選擇靜態或動態快捷方式功能表方法。
title: 選擇靜態或動態快捷方式功能表方法
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: dfd73ee052594e1136fe2885ce92b682f229096b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394773"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>選擇靜態或動態快捷方式功能表方法

本主題的組織方式如下：

-   [選擇動詞方法](#choose-a-verb-method)
    -   [靜態動詞方法](#static-verb-methods)
    -   [慣用動態動詞方法](#preferred-dynamic-verb-methods)
    -   [不建議的動態動詞方法](#discouraged-dynamic-verb-methods)
-   [擴充快捷方式功能表](#extend-a-shortcut-menu)
-   [依作業系統支援動詞方法](#support-for-verb-methods-by-operating-system)
-   [相關主題](#related-topics)

## <a name="choose-a-verb-method"></a>選擇動詞方法

強烈建議您使用其中一個靜態動詞方法來執行快捷方式功能表。

### <a name="static-verb-methods"></a>靜態動詞方法

靜態動詞是最簡單的動詞命令，但是它們仍提供豐富的功能。 請一律選擇符合您需求的最簡單快捷方式功能表方法。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>靜態動詞</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>使用命令列參數的<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a></td>
<td>這是實作為靜態動詞命令的最簡單且最常見的方法。 處理常式是透過對 <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> 函式的呼叫來叫用，並以選取的檔案和任何選擇性參數傳遞做為命令列。 這會開啟檔案或資料夾。<br/> 此方法具有下列限制：
<ul>
<li>命令列長度限制為2000個字元，這會限制動詞可以處理的專案數。</li>
<li>只能搭配檔案系統專案使用。</li>
<li>不允許重複使用已在執行中的進程。</li>
<li>需要安裝可執行檔才能處理動詞。</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DropTarget</strong> /<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></td>
<td>以 COM 為基礎的動詞啟用表示支援進程內或跨進程啟用。 <strong>DropTarget</strong> /當本機伺服器執行<strong>IDropTarget</strong>介面時， <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>也支援重複使用已在執行中的處理常式。 它也會透過封送處理的資料物件完全表示專案，並提供叫用網站鏈的參考，讓您可以透過 <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>與啟動程式互動。</td>
</tr>
<tr class="odd">
<td>Windows 7 和更新版本： <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></td>
<td>最直接的實作為方法。 因為這是以 COM 為基礎的叫用方法 (像是 DropTarget) 這個介面支援進程內部和跨進程啟用。 此動詞命令會執行 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>，並選擇性地 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>。 這些專案會直接傳遞為 Shell 專案陣列，而來自啟動程式的更多參數則可用於動詞執行，包括叫用點、鍵盤狀態等等。</td>
</tr>
<tr class="even">
<td>Windows 7 和更新版本：<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></td>
<td>啟用透過 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> 提供命令模組命令的資料來源，以使用這些命令做為快捷方式功能表上的動詞命令。 因為這個介面僅支援同進程啟用，所以建議您在命令和快捷方式功能表之間必須共用執行的 Shell 資料來源使用。</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 是靜態和動態動詞之間的混合式。 **IExplorerCommand** 是在 windows Vista 中宣告，但它在快捷方式功能表中執行動詞的能力是 windows 7 的新功能。

 

如需檔案關聯屬性之 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 和 Shell 查詢的詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。

### <a name="preferred-dynamic-verb-methods"></a>慣用動態動詞方法

慣用的動態動詞方法如下：



| 動詞類型                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 上表中所列的靜態動詞命令 () + Advanced 查詢語法 (AQS)                   | 此選項會取得動態動詞可視性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 和更新版本： [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | 此選項可讓您在 Windows 檔案總管的命令模組中顯示動詞和 explorer 命令的一般執行。                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 和更新版本： [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + 靜態動詞 | 這種選擇也會取得動態動詞的可見度。 它是一種混合式模型，其中會使用簡單的同進程處理常式來計算是否應該 displyed 指定的靜態動詞。 這可套用至所有的靜態動詞命令實方法，以達成動態行為，並將同進程邏輯的曝光降至最低。 [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) 具有在背景執行緒上執行的優點，因此可避免 UI 停止回應。 它比 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)簡單得多。 |



 

### <a name="discouraged-dynamic-verb-methods"></a>不建議的動態動詞方法

[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 是最強大的功能，但也是最複雜的方法來執行。 它是以在呼叫端執行緒上執行的同進程 COM 物件為基礎，這通常會 Windows 檔案總管，但可以是裝載專案的任何應用程式。 **ICoNtextMenu** 支援動詞可見度、排序和自訂繪圖。 其中有些功能已新增至靜態動詞功能，例如與命令相關聯的圖示，以及 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 來處理可見度。

如果您必須註冊檔案類型的動態動詞命令以擴充檔案類型的快捷方式功能表，請依照 [使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)中提供的指示進行。

## <a name="extend-a-shortcut-menu"></a>擴充快捷方式功能表

選擇動詞方法之後，您可以註冊檔案類型的靜態動詞命令，以擴充檔案類型的快捷方式功能表。 如需詳細資訊，請參閱 [建立快顯功能表處理常式](context-menu-handlers.md)。

## <a name="support-for-verb-methods-by-operating-system"></a>依作業系統支援動詞方法

下表列出對動詞調用方法的支援（依作業系統）。



| Verb 方法          | Windows XP | Windows Vista | Windows 7 和以上 |
|----------------------|------------|---------------|----------------------|
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| ExecuteCommand       |            | X             | X                    |
| ExplorerCommand      |            |               | X                    |
| ExplorerCommandState |            |               | X                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速鍵功能表處理常式和多重選取動詞的最佳作法](verbs-best-practices.md)
</dt> <dt>

[建立快捷方式功能表處理常式](context-menu-handlers.md)
</dt> <dt>

[使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[快捷方式 (內容) 功能表和快捷方式功能表處理常式](context-menu.md)
</dt> <dt>

[快速鍵功能表參考](context-menu-reference.md)
</dt> <dt>

[動詞和檔案關聯](fa-verbs.md)
</dt> </dl>

 

 
