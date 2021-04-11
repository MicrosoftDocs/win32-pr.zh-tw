---
description: HRECOCONTEXT 控制碼是用來將筆墨新增至內容、以同步或非同步方式執行筆墨辨識 () 、取出辨識結果，以及抓取替代項。
ms.assetid: 509188e2-28af-4915-bc76-ee451133398f
title: 'HRECOCONTEXT 控制碼 (Recapis .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef2b6f629587de84f831fd32a31f42a208c024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848099"
---
# <a name="hrecocontext-handle"></a>HRECOCONTEXT 控制碼

**HRECOCONTEXT** 控制碼是用來將筆墨新增至內容、以同步或非同步方式執行筆墨辨識 () 、取出辨識結果，以及抓取替代項。

具有辨識器內容控制碼的主要原因是要區分筆跡輸入。 例如，您可以建立具有兩個視窗的應用程式，使用者可以在任一視窗中進行筆跡。 當您要求辨識器辨識其中一個視窗的筆墨時，不希望第一個視窗的筆墨與第二個視窗的筆墨混合。 在這種類型的應用程式中，您會建立兩個辨識器內容 (每個視窗) 一個，並將進入視窗1的筆觸加入至辨識器內容1，並將視窗2中的筆觸新增至辨識器內容2。 若要傳回辨識結果，請根據您想要的是視窗1或2的結果，呼叫辨識器內容1或辨識器內容2上的進程。

辨識器內容控制碼可以是您想要的任何內容。 但一般而言，它是結構全域陣列中的索引。 這些結構可能包含已輸入的所有筆劃，以及辨識器針對該特定筆跡所使用的所有變數 (例如，您的內部 >lattice 結構或辨識) 的目前狀態。 其中一個結構可能包含辨識器所需的所有資訊，並用於一段特定的筆跡。

若要取得 **HRECOCONTEXT** 控制碼，請呼叫 [**CreateCoNtext**](/windows/desktop/api/recapis/nf-recapis-createcontext) 函數。


```C++
typedef HANDLE HRECOCONTEXT;
```



## <a name="remarks"></a>備註

下列是 **HRECOCONTEXT** 函式



| 函式                                                            | 描述                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStroke**](/windows/desktop/api/recapis/nf-recapis-addstroke)                                      | 將筆墨筆劃新增至辨識器內容。<br/>                                                                                                                                                                                                    |
| [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange)                          | 停止辨識器處理筆墨，因為正在新增或刪除新的筆劃。<br/>                                                                                                                                                         |
| [**CloneCoNtext**](/windows/desktop/api/recapis/nf-recapis-clonecontext)                                | 建立辨識器內容，其中包含與原始相同的設定。 新的辨識器內容不包含原始的筆墨或辨識結果。<br/>                                                                        |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)             | 表示內容中不會再加入任何筆墨。<br/>                                                                                                                                                                                         |
| [**GetAlternateList**](/previous-versions/windows/desktop/legacy/ms698163(v=vs.85))                        | 傳回最佳結果字串的替代清單。<br/>                                                                                                                                                                                         |
| [**GetBestAlternate**](/previous-versions/windows/desktop/legacy/ms699575(v=vs.85))                        | 傳回 [HRECOALT 控制碼](hrecoalt-handle.md) 指標，以取得最佳的結果替代。<br/>                                                                                                                                                         |
| [**GetBestResultString**](/windows/desktop/api/recapis/nf-recapis-getbestresultstring)                  | 傳回最佳的結果字串。<br/>                                                                                                                                                                                                                  |
| [**GetCoNtextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)            | 傳回辨識器所支援的屬性清單。<br/>                                                                                                                                                                                            |
| [**GetCoNtextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)          | 從辨識器內容傳回指定的屬性值。<br/>                                                                                                                                                                                  |
| [**GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)          | 傳回在內容上啟用的 Unicode 點範圍清單。<br/>                                                                                                                                                                                   |
| [**GetGuide**](/windows/desktop/api/recapis/nf-recapis-getguide)                                        | 傳回用於裝箱或線條輸入的指南。<br/>                                                                                                                                                                                                 |
| [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)                              | 傳回目前結果的 >lattice 指標。<br/>                                                                                                                                                                                        |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) | 傳回值，這個值表示字典中是否包含文字、日期、時間、數位或傳入的其他文字。<br/>                                                                                                               |
| [**處理序**](/windows/desktop/api/recapis/nf-recapis-process)                                          | 以同步方式執行手寫辨識。<br/>                                                                                                                                                                                                          |
| [**ResetCoNtext**](/windows/desktop/api/recapis/nf-recapis-resetcontext)                                | 從內容中刪除目前的筆墨和辨識結果。<br/>                                                                                                                                                                                |
| [**SetCACMode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)                                    | 指定字元或字組識別的字元自動完成模式。<br/>                                                                                                                                                                         |
| [**SetCoNtextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)          | 將屬性新增至辨識器內容。 如果屬性已經存在，則會修改它的值。<br/>                                                                                                                                                  |
| [**SetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)          | 啟用內容上的一個或多個 Unicode 點範圍。<br/>                                                                                                                                                                                         |
| [**SetFactoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)                                    | 設定辨識器用來限制其搜尋結果的模擬程式。<br/>                                                                                                                                                                       |
| [**SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)                                        | 設定辨識器如何解讀筆墨並決定結果字串。<br/>                                                                                                                                                                     |
| [**SetGuide**](/windows/desktop/api/recapis/nf-recapis-setguide)                                        | 設定用於已裝箱或線條輸入的指南。<br/>                                                                                                                                                                                                  |
| [**SetTextCoNtext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)                            | 提供在辨識器內容中包含的文字之前和之後的文字字串。 對於東亞字元的辨識器， [**SetTextCoNtext**](/windows/desktop/api/recapis/nf-recapis-settextcontext) 函式會提供字元而非文字字串。<br/> |
| [**SetWordList**](/windows/desktop/api/recapis/nf-recapis-setwordlist)                                  | 將目前辨識器內容的單字清單設定為可辨識。<br/>                                                                                                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                        |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>Recapis。h</dt> </dl> |



 

