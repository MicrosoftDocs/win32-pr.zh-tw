---
description: 以下是 sequence 資料表的範例。
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: 順序資料表詳細範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc6e9715850d05231080cd8cd832ac7f39c1e3044628bb307afb51bf92c2210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040188"
---
# <a name="sequence-table-detailed-example"></a>順序資料表詳細範例

以下是 sequence 資料表的範例。



| 動作                                          | 條件                                                       | 順序 |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md) |                                                                 |          |
| [AppSearch](appsearch-action.md)               |                                                                 | 200      |
| [CCPSearch](ccpsearch-action.md)               | CCP \_ 測試                                                       | 300      |
| CCPDialog                                       | 不是 \_ CCP \_ 成功                                               | 400      |
| MyCustomConfig                                  | 未 [**安裝**](installed.md)                              | 500      |
| [CostInitialize](costinitialize-action.md)     |                                                                 | 600      |
| [FileCost](filecost-action.md)                 |                                                                 | 700      |
| [CostFinalize](costfinalize-action.md)         |                                                                 | 800      |
| >installdialog                                   | 未 [**安裝**](installed.md)                              | 900      |
| MaintenanceDialog                               | [**已安裝**](installed.md) 而不是 [**繼續**](resume.md) | 1000     |
| ActionDialog                                    |                                                                 | 1100     |
| [RegisterProduct](registerproduct-action.md)   |                                                                 | 1200     |
| [InstallValidate](installvalidate-action.md)   |                                                                 | 1300     |
| [InstallFiles](installfiles-action.md)         |                                                                 | 1400     |
| MyCustomAction                                  | $MyComponent > 2                                             | 1500     |
| [InstallFinalize](installfinalize-action.md)   |                                                                 | 1600     |



 

此順序表中的下列動作是由安裝程式所定義，而且是標準動作的範例：

[LaunchConditions](launchconditions-action.md)

 

[AppSearch](appsearch-action.md)

 

[CCPSearch](ccpsearch-action.md)

 

[CostInitialize](costinitialize-action.md)

 

[FileCost](filecost-action.md)

 

[CostFinalize](costfinalize-action.md)

 

[RegisterProduct](registerproduct-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallValidate](installvalidate-action.md)

下列動作是由資料表的作者所定義，而且是 [自訂動作](custom-actions.md) 的範例，而且必須列在 [CustomAction 資料表](customaction-table.md)中：

MyCustomConfig

 

MyCustomAction

[動作] 欄位中的其餘專案是 [對話方塊資料表](dialog-table.md)中的外鍵。 如果條件欄位評估為 True，則會指定將顯示之對話方塊的名稱。

CCPDialog

 

>installdialog

 

MaintenanceDialog

 

ActionDialog

如果此欄位中的屬性或運算式為 False，則 [條件] 資料行會讓安裝程式略過該動作。 [**已安裝**](installed.md)的屬性和 [**RESUME**](resume.md)屬性是安裝程式所設定之屬性的範例。 如果已安裝產品，則已 [**安裝**](installed.md) 的屬性會設定為 true，如果繼續已暫停的安裝，則會設定 [**RESUME**](resume.md) 屬性。 CCP \_ 測試和 NOT \_ CCP \_ SUCCESS 屬性是可在使用者安裝應用程式時于命令列設定的屬性範例。

所有動作都會依序執行，並具有下列條件式步驟：

-   只有在已設定 CCP 測試時，才會執行 CPPSearch \_ 。
-   只有在未設定 [CCP SUCCESS] 時，才會執行 CCPDialog \_ \_ 。
-   只有在已安裝此產品，且這不是在暫停後繼續執行的安裝時，才會執行 MaintenanceDialog。
-   只有當 Condition 資料行中的運算式為 True 時，才會執行 MyCustomAction。 運算式 $MyComponent > 2 是指稱為 MyComponent 的元件的動作狀態。 此條件表示 MyCustomAction 只有在 MyComponent 設定為已安裝時才應該執行。 如需動作狀態和選取狀態的詳細資訊，請參閱 [**FeatureRequestState**](session-featurerequeststate.md) 屬性、 [功能資料表](feature-table.md)和 [InstallFiles 動作](installfiles-action.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用屬性](using-properties.md)
</dt> <dt>

[條件陳述式語法](conditional-statement-syntax.md)
</dt> </dl>

 

 



