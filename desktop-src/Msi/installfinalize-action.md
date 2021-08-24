---
description: InstallFinalize 動作會執行腳本，其中包含自安裝開始或執行 InstallExecute 或 InstallExecuteAgain 動作之後，動作順序中的所有作業。
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: InstallFinalize 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8bd3ac9473fab868e5f7d83e760b39ca4dd6136faec987b5a7d2a3777bdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787038"
---
# <a name="installfinalize-action"></a>InstallFinalize 動作

InstallFinalize 動作會執行腳本，其中包含自安裝開始或執行 [InstallExecute](installexecute-action.md) 或 [InstallExecuteAgain](installexecuteagain-action.md) 動作之後，動作順序中的所有作業。 此動作會標示以 [InstallInitialize](installinitialize-action.md) 動作開頭的交易結尾。

## <a name="sequence-restrictions"></a>順序限制

[InstallInitialize](installinitialize-action.md)動作必須位於 InstallFinalize 動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

如果偵測到產品已標示為要完成移除，則會自動將作業新增至腳本，以移除產品 **主控台** 資訊中的 [**新增/移除程式**]、取消註冊並解除發佈產品，以及從% WINDOWS% 移除快取的本機資料庫（如果有的話）。

執行 InstallFinalize 動作之後，在動作之前所做的系統變更可能不會還原。 InstallFinalize 動作會將已判斷為該點的所有作業更新為系統，然後結束交易。

 

 



