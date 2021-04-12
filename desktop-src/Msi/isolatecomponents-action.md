---
description: IsolateComponents 動作會將元件的複本安裝 (通常是共用 DLL) 至私用位置，以供特定應用程式使用， (通常是 .exe) 。
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: IsolateComponents 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320568"
---
# <a name="isolatecomponents-action"></a>IsolateComponents 動作

IsolateComponents 動作會將元件的複本安裝 (通常是共用 DLL) 至私用位置，以供特定應用程式使用， (通常是 .exe) 。 這會將應用程式與元件的其他複本隔離，以安裝到電腦上的共用位置。 如需詳細資訊，請參閱 [獨立元件](isolated-components.md)。

此動作會參考 [IsolatedComponent 資料表](isolatedcomponent-table.md) 的每一筆記錄，並將 [元件共用] 欄位中所列元件的檔案 \_ 與 [元件應用程式] 欄位中所列的元件產生關聯 \_ 。 安裝程式會將共用的元件檔案安裝 \_ 到與元件應用程式相同的目錄中 \_ 。 安裝程式會在此目錄中產生檔案（長度為零個位元組），為元件應用程式使用金鑰檔的簡短檔案名， \_ (通常這與 .exe) 附加的檔案名相同。 IsolatedComponent 動作不會影響元件應用程式的安裝 \_ 。 卸載元件 \_ 應用程式也會 \_ 從目錄中移除元件共用檔案和本機檔案。

## <a name="sequence-restrictions"></a>順序限制

IsolateComponents 動作只能用在 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。 此動作必須在 [CostInitialize 動作](costinitialize-action.md) 之後，以及 [CostFinalize 動作](costfinalize-action.md)之前。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

如果 [IsolateComponents] 動作的 [條件] 資料行評估為 True，或保留空白，則安裝程式會隔離 [IsolatedComponent 資料表](isolatedcomponent-table.md)中所列的所有元件。 如果 [條件] 資料行評估為 False，則安裝程式會忽略 IsolatedComponent 資料表並照常共用這些元件。 [**RedirectedDllSupport**](redirecteddllsupport.md)屬性可用來條件執行此動作。 如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

 

 



