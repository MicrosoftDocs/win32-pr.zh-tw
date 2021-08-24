---
description: ICE83 會驗證 MsiAssembly 資料表。
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e8014f8feee76e4d1910fb601e186bec928a0fd6d6d34469ce2c2b201b724d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580748"
---
# <a name="ice83"></a>ICE83

ICE83 會驗證 [MsiAssembly 資料表](msiassembly-table.md)。 如果包含 Win32 元件之元件的金鑰路徑設定為資訊清單檔，此 ICE 自訂動作會張貼錯誤。 如果在 [元件資料表](component-table.md) 的 [KeyPath] 欄位中輸入的值等於 [MsiAssembly] 資料表的 [檔案資訊清單] 欄位中輸入的值，就會明確地公佈錯誤 \_ 。 如果 MsiAssembly 資料表中至少有一筆記錄，而且 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 不包含 [MsiPublishAssemblies 動作](msipublishassemblies-action.md) 和 [MSIUNPUBLISHASSEMBLIES 動作](msiunpublishassemblies-action.md)，則此 ICE 自訂動作會張貼錯誤。

## <a name="result"></a>結果

ICE83 會張貼下列錯誤。



| ICE83 錯誤                                                                                                   | 描述                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Win32 SXS 元件的金鑰路徑 (元件 \_ = \[ 1 \]) 不能是其資訊清單檔                       | 當 Win32 元件的 KeyPath 欄位設定為其資訊清單檔時，ICE83 會將此錯誤張貼 (元件。 KeyPath = = MsiAssembly。檔案 \_ 資訊清單) 。 \[1 \] 是元件資料表中的 KeyPath                          |
| MsiPublishAssemblies 和 MsiUnpublishAssemblies 動作都必須存在於 InstallExecuteSequence 資料表中。 | ICE83 會在 MsiAssembly 資料表中至少有一個專案時張貼此錯誤，但 InstallExecuteSequence 資料表不包含 MsiAssemblyPublish 動作和 MsiAssemblyUnpublish 動作。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



