---
description: 如果 MOF 編譯器無法完成 MOF 檔案的編譯，WMI 儲存機制可能會處於未定義狀態。
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: 使用 MOF 編譯器處理錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f5174af836a0b27824c40486364cc81809db97b9608e6b1c813c4c1029d3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993168"
---
# <a name="handling-errors-with-the-mof-compiler"></a>使用 MOF 編譯器處理錯誤

如果 MOF 編譯器無法完成 MOF 檔案的編譯，WMI 儲存機制可能會處於未定義狀態。 例如，如果您要編譯 MOF 檔案，且使用 **-class：以** 命令列參數，則編譯會在 MOF 檔案中指定的類別已存在時終止。 MOF 編譯器會將任何定義的類別或實例儲存在存放庫中，直到編譯器停止為止。 在某些情況下，這可能會讓 WMI 存放庫處於未定義的情況。

在這種情況下，您可能需要停止 WMI、刪除 WMI 儲存機制，並讓 WMI 重建它。 當 WMI 重新開機時，會重建包含 [**pragma 自動**](pragma-autorecover.md)回復 [預處理器命令](preprocessor-commands.md) 的所有 MOF 檔案。 您必須手動重新編譯任何不包含語句的 MOF 檔案 `#pragma autorecover` 。

如需如何使用 MOF 語法宣告類別和實例的詳細資訊，請參閱 [設計受控物件格式 (mof) 類別](designing-managed-object-format--mof--classes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編譯 MOF 檔案](compiling-mof-files.md)
</dt> <dt>

[**mofcomp.exe**](mofcomp.md)
</dt> <dt>

[預處理器命令](preprocessor-commands.md)
</dt> </dl>

 

 



