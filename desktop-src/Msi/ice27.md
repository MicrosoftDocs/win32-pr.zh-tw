---
description: ICE27 會驗證安裝套件的順序資料表，以取得搜尋、成本、選取和執行區段中的有效動作、動作順序限制和組織。
ms.assetid: c5292a3c-57bb-4203-96a1-6d747f554178
title: ICE27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb4b90b313f5f78874fb93ce9d32c3650b97064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848779"
---
# <a name="ice27"></a>ICE27

ICE27 會驗證安裝套件的 [*順序資料表*](s-gly.md) ，以取得搜尋、成本、選取和執行區段中的有效動作、動作順序限制和組織。

ICE27 自訂動作會驗證下列各項：

-   順序資料表之 [動作] 資料行中所列的動作是 [標準動作](standard-actions.md)、 [CustomAction 資料表](customaction-table.md)中所列的自訂動作，或 [對話方塊資料表](dialog-table.md)中所列的對話方塊。
-   受限於排序限制的動作，在動作順序中的相對順序都是正確的。 當某個動作相依于另一個動作時，排序限制結果。
-   限制為序列特定區段的動作位於其所屬的位置。 ICE27 會驗證下列順序資料表組織。 請注意，並非每個順序資料表都有每個區段。 請參閱 [使用順序資料表](using-a-sequence-table.md)中的建議順序資料表。



| 順序資料表區段 | 動作順序中的範圍                                                                       | 屬於區段的動作                                                                                                                                                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 搜尋                 | {start} 至 [CostInitialize](costinitialize-action.md)                                         | 搜尋現有應用程式的動作。 [AppSearch](appsearch-action.md)<br/> [CCPSearch](ccpsearch-action.md)<br/>                                                                                                         |
| 成本                | [CostInitialize](costinitialize-action.md) 至 [CostFinalize 動作](costfinalize-action.md)  | 執行檔案 [成本](file-costing.md)的動作。 [CostInitialize](costinitialize-action.md)<br/> [FileCost](filecost-action.md)<br/> [CostFinalize](costfinalize-action.md)<br/>                                           |
| 選取              | [CostFinalize](costfinalize-action.md) 至 [InstallValidate](installvalidate-action.md)       | 設定資料夾或功能狀態的動作。 [SetODBCFolders 動作](setodbcfolders-action.md)<br/>                                                                                                                                        |
| 執行              | [InstallValidate](installvalidate-action.md) 至 [InstallFinalize](installfinalize-action.md) | 腳本動作，例如註冊、發行集、安裝 (複製) 的檔案。 請注意，只有在執行區段中有動作時， [InstallFinalize 動作](installfinalize-action.md) 才必須在資料表中。<br/> |
| PostExecution          | [InstallFinalize](installfinalize-action.md) 至 {end}                                         | [RemoveExistingProducts](removeexistingproducts-action.md)                                                                                                                                                                                      |



 

ICE27 會驗證下列資料表：

-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>結果

如果封裝中的順序資料表具有不正確動作順序或組織，ICE27 會張貼一則錯誤訊息。

## <a name="example"></a>範例



| ICE27 錯誤                                                                                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 未知的動作： InstallExecuteSequnence 資料表的 ' Action1 '。 不是標準的動作，而且在 CustomAction 或對話方塊資料表中找不到    | 順序資料表中所列的動作指出不是 [標準動作](standard-actions.md)、 [CustomAction 資料表](customaction-table.md)中所列的自訂動作，或 [對話方塊資料表](dialog-table.md)中所列的對話方塊。                                                                                                                                                                                                                                                                       |
| InstallExecute 資料表中的 ' Action2 ' 發生錯誤。 最新：搜尋、正確：成本                                                 | 順序資料表中的動作，與 Sequence 資料行中的序號不正確地放在一起。 「目前」表示在指定的順序資料表的搜尋、成本、選取或執行區段中，動作目前的位置。<br/> 「正確」表示動作所屬的區段。<br/> 若要修正這個錯誤，請將動作的序號變更為正確區段內的序號。 請注意，某些動作可以在一個以上的區段中找到。<br/> |
| 只有在執行腳本作業時，才能呼叫 InstallExecuteSequence 資料表中的 ' InstallFinalize ' 動作             | 順序資料表中有一個 [InstallFinalize 動作](installfinalize-action.md) ，在資料表的 [執行] 區段中不包含任何腳本作業。 將動作加入至執行區段，或從資料表中移除 InstallFinalize 動作。<br/>                                                                                                                                                                                                                                                        |
| 必須在 InstallExecuteSequence 資料表中呼叫 InstallFinalize，因為腳本作業存在於執行中                            | 有一個順序資料表包含執行區段中不包含 [InstallFinalize 動作](installfinalize-action.md)的動作。 將 InstallFinalize 動作新增至此順序資料表，並為其指定最大的序號，以將其放在動作順序中的最後一個。<br/>                                                                                                                                                                                                                            |
| Action： InstallExecuteSequence 資料表中的 ' Action3 ' 必須在 ' Action5 ' 動作之前。 目前 \# 的 seq：1200。 相依 seq \# ：1100 | 在指定的順序資料表中，有一個在相依動作之後排序的動作。 變更相依動作的序號，使其出現在動作之前。<br/>                                                                                                                                                                                                                                                                                                                                    |
| Action： InstallExecuteSequence 資料表中的 ' Action4 ' 必須在 ' Action6 ' 動作之後。                                             | 在指定的順序資料表中，有一個動作會在其相依的動作之前排序。 變更動作的序號，使其在其相依動作之後。<br/>                                                                                                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




