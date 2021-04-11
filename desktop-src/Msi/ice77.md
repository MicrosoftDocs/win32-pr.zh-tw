---
description: ICE77 會確認 msidbCustomActionTypeInScript 位集的自訂動作是否會在 InstallInitialize 動作之後，以及 InstallFinalize 動作之前排序。
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113856"
---
# <a name="ice77"></a>ICE77

ICE77 會確認 **msidbCustomActionTypeInScript** 位集的自訂動作是否會在 [InstallInitialize 動作](installinitialize-action.md) 之後，以及 [InstallFinalize 動作](installfinalize-action.md)之前排序。 ICE77 會檢查 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 和 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)中的順序。

## <a name="result"></a>結果

如果腳本內自訂動作是在 InstallInitialize 動作之前或 InstallFinalize 動作之後排序，ICE77 會張貼錯誤。

ICE77 會在 InstallInitialize 動作或 InstallFinalize 動作遺失時張貼錯誤。

## <a name="example"></a>範例

ICE77 會報告範例的下列錯誤：

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

[CustomAction 資料表](customaction-table.md) (部分) 



| 動作              | 類型 |
|---------------------|------|
| CA \_ InScriptInstall | 1025 |
| CA \_ InScriptAdmin   | 1026 |



 

[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) 



| 動作              | 順序 |
|---------------------|----------|
| CA \_ InScriptInstall | 2000     |
| InstallInitialize   | 1500     |



 

[AdminExecuteSequence 資料表](adminexecutesequence-table.md) (部分) 



| 動作            | 順序 |
|-------------------|----------|
| CA \_ InScriptAdmin | 1400     |
| InstallInitialize | 1500     |
| InstallFinalize   | 6600     |



 

若要修正錯誤，請在 InstallInitialize 動作之後以及 InstallFinalize 動作之前，將腳本內自訂動作排序。 InstallInitialize 和 InstallFinalize 動作必須存在於 InstallExecuteSequence 資料表和 AdminExecuteSequence 資料表中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



