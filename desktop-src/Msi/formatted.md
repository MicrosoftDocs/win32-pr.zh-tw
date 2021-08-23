---
description: 格式化的資料類型是一種文字字串，可進行處理以解析內嵌的屬性名稱、資料表索引鍵、環境變數參考和其他特殊子字串。
ms.assetid: 7a1bc160-a06c-4d57-b429-e39167893a45
title: 已格式化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58cd21a53a3f77a646d6da0fac04480bd709ab8f1d7ddcb918d5362a0a366c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649638"
---
# <a name="formatted"></a>已格式化

格式化的資料類型是一種文字字串，可進行處理以解析內嵌的屬性名稱、資料表索引鍵、環境變數參考和其他特殊子字串。 下列慣例可辨識為可解析字串：

-   括弧 (\[ \]) 或大括弧 ( {} ) 沒有相符的配對會留在文字中。
-   如果遇到了格式 propertyname 的子字串 \[  \] ，就會由屬性的值取代。 如果 *propertyname* 不是有效的屬性名稱，則子字串會解析為空白。 例如， [LaunchCondition 資料表](launchcondition-table.md) 的 Description 資料行採用格式化的字串。 如果 ERRORTXT 已設定為「請洽詢您的支援人員」。 然後，針對啟動條件失敗所顯示的文字會包含這個字串。 如果未設定 ERRORTXT，則顯示為啟動狀況失敗的文字會是「系統不符合安裝需求」。

    

    | 條件 | 描述                                                  |
    |-----------|--------------------------------------------------------------|
    | Version9X | 系統不符合安裝需求。 \[ERRORTXT\] |

    

     

-   可以逐一查看方括弧，並從內部解析屬性名稱。例如，假設子字串 \[ \[ PropertyA \] \] 出現在文字中。 首先，會取出屬性 PropertyA 的值。 如果此值是有效的屬性名稱（例如 PropertyB），則會抓取 PropertyB 的值，而整個子字串 \[ \[ PropertyA \] \] 會取代為 PropertyB 的值。 如果 PropertyA 不是有效的屬性名稱，或 PropertyA 的值不是有效的屬性名稱，則子字串會空白。
-   如果找到 environmentvariable 格式的子字串 \[ %  \] ，則會將環境變數的值取代為子字串。
-   如果找到 x 格式的子字串，則會將 \[ \\  \] 它取代為字元 *x* ，其中 *x* 是一個字元，不需要任何進一步的處理。 只保留反斜線之後的第一個字元;所有其他專案都已移除。 例如，若要在) 中包含常值左括弧 (\[ ，請使用 \[ \\ \[ \] 。 文字 \[ \\ \[ \] 括弧文字會 \[ \\ \] \] 解析成 \[ 括弧文字 \] 。
-   如果子字串以大括弧括住 ( {} ) ，而且未包含以方括弧括住的屬性名稱 (\[ \]) ，則子字串會保持不變，包括大括弧。
-   如果子字串是以大括弧括住 ( {} ) 而且它包含一個或多個以方括弧括住的屬性名稱 (\[ \]) 然後，如果所有的屬性名稱都有效，則會顯示具有已解析之替換 (的文字) ，但不含大括弧。
-   如果找到表單的子字串，則會 \[ ~ \] 以 null 字元取代。 這是用來在登錄 [資料表](registry-table.md)中撰寫 **REG \_ 多重 \_ SZ** 字元字串。 請注意，您 \[ ~ \] 也可以使用[環境資料表](environment-table.md)，將值附加至環境變數或將其前置詞。
-   如果找到 filekey 格式的子字串，則會以檔案的 \[ \#  \] 完整路徑來取代它，而值 *filekey* 會用來做為檔案 [資料表](file-table.md)中的索引鍵。 Filekey 的值 \[ \#  \] 會保持空白，而且在安裝程式執行[CostInitialize 動作](costinitialize-action.md)、 [FileCost 動作](filecost-action.md)和[CostFinalize 動作](costfinalize-action.md)之前，不會由路徑取代。 Filekey 的值 \[ \#  \] 取決於檔案所屬元件的安裝狀態。 如果元件是從來源執行，則此值為檔案來源位置的路徑。 如果元件是在本機執行，則此值是安裝之後檔案目標位置的路徑。 如果元件的動作狀態為 [不存在]，則會使用元件的已安裝狀態來決定 \[ \) 。
-   如果找到 componentkey 格式的子字串 \[ $  \] ，就會由元件的安裝目錄取代，並以值 *componentkey* 做為 [元件資料表](component-table.md)中的索引鍵。 Componentkey 的值 \[ $  \] 會保持空白，而且在安裝程式執行[CostInitialize 動作](costinitialize-action.md)、 [FileCost 動作](filecost-action.md)和[CostFinalize 動作](costfinalize-action.md)之前，不會以目錄取代。 Componentkey 的值 \[ $  \] 取決於元件的安裝狀態及其發生位置。 在登錄 [資料表](registry-table.md)的 [值] 資料行中，這個子字串可能會參考此元件的動作狀態或要求的動作狀態。 在其他所有情況下，這個子字串是指元件的動作狀態。 例如，如果元件是從來源執行，則此值為檔案的來原始目錄。 如果元件是在本機執行，則在安裝之後，此值會是目標目錄。 如果元件不存在，此值會保留空白。 Windows安裝程式會追蹤元件的動作和要求的安裝狀態。 例如，如果已安裝元件，它可能會有本機的要求狀態，以及 null 的動作狀態。 如需有關檢查元件安裝狀態的詳細資訊，請參閱 [檢查功能、元件、](checking-the-installation-of-features-components-files.md)檔案的安裝。
-   請注意，如果元件已安裝，且未在目前安裝期間重新安裝、移除或移動，則元件的動作狀態為 null，且字串 \[ $ *componentkey* 會 \] 評估為 null。
-   如果表單的子字串 \[ ！*filekey* \] 找到，它會取代為檔案的完整短路徑，而值 *filekey* 會用來做為檔案 [資料表](file-table.md)中的索引鍵。

    只有在登錄或 IniFile 資料表的 Value 資料行中使用此語法時，此語法才有效。 在其他資料行中使用時，此語法會視為與 \[ \# *filekey* 相同 \] 。

 

 



