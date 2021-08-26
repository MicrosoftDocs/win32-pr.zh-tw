---
description: 安裝套件的作者應該一律先在封裝上執行驗證，再嘗試第一次安裝套件，並在對套件進行任何變更時重新執行驗證。
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: 驗證安裝資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28d4d1937b5946d6c1df85a4c6c21ec8113ef6463b5aaad0e181f4bdc711e70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995818"
---
# <a name="validating-an-installation-database"></a>驗證安裝資料庫

安裝套件的作者應該一律先在封裝上執行驗證，再嘗試第一次安裝套件，並在對套件進行任何變更時重新執行驗證。 驗證會掃描資料庫的錯誤，這些錯誤可能會個別出現，但在整個資料庫的內容中造成不正確的行為。 嘗試安裝驗證失敗的封裝可能會損毀使用者的系統。 請參閱 [套件驗證](package-validation.md) 和 [內部一致性評估](internal-consistency-evaluators-ices.md)工具的章節。

您可以使用 [Orca.exe](orca-exe.md) 或 [Msival2.exe](msival2-exe.md)來驗證範例封裝。 若要查看 Msival2.exe 變更目錄的說明，並在命令列上輸入。

Msival2 -?

.Cub 檔 darice 包含 Msival2.exe 執行驗證所需的 ICE 自訂動作。 若要驗證 MNP2000.msi 輸入

msival2 MNP2000.msi Darice .cub

如需驗證所傳回之錯誤和警告訊息的說明，請參閱 [ICE 參考](ice-reference.md)。 更正封裝中的所有錯誤，並視需要重新執行驗證，直到封裝通過驗證而沒有錯誤。

當套件通過驗證之後，您可以按一下 MNP2000.msi 圖示，或從命令列使用 [命令列選項](command-line-options.md)來安裝範例封裝。

這會完成範例安裝。

## <a name="next-example"></a>下一個範例

[升級範例](an-upgrade-example.md)

 

 



