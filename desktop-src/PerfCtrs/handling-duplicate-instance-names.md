---
description: 雖然我們鼓勵提供者使用唯一的實例名稱，但並非所有提供者都能使用。
ms.assetid: 3c8fcb8d-2ea4-4b24-b649-7bd375c1133d
title: 處理重複的實例名稱
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 220e5d7d0181a79c1d1415486cc946d484e11952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998500"
---
# <a name="handling-duplicate-instance-names"></a>處理重複的實例名稱

雖然強烈建議您使用提供者來使用唯一的實例名稱，但並非所有提供者都有提供。 顯示重複實例名稱的慣例是將 `#` 字元和序號附加至實例名稱，但不包括第一次出現的名稱。 例如，如果範例中有三個實例 `svchost` ，則會將三個名稱顯示為 `svchost` 、 `svchost#1` 和 `svchost#2` 。

可惜的是，這個慣例並不能完全解決問題。 序號是根據特定實例名稱在範例中出現的順序來指派，且此順序可能會與樣本範例不一致。 例如，範例 A 可能會看到 `svchost` (pid 100) 、 `svchost#1` (pid 200) 和 `svchost#2` (PID 300) 。 然後，如果具有 PID 100 的 svchost 關機，則下一個範例會看到 `svchost` (pid 200) 和 `svchost#1` (pid 300) 。 基本相符邏輯會嘗試將範例 A 的 `svchost#1` 統計資料從 pid 200)  (與 pid 300) 所 (的範例 b 統計資料相符 `svchost#1` ，導致範例 b 的結果無效。在範例中出現新的非唯一實例時，或如果已新增/移除的實例是最後一個 (，就會發生錯誤。

## <a name="process-counterset"></a>進程 counterset

這個問題對 counterset 特別有問題， `Process` 因為它只會使用進程的 exe 名稱做為實例名稱，即使 EXE 名稱不是唯一的也是一樣。 `Process`因為相容性問題，所以無法變更 Windows 上的 counterset 預設行為。

您可以藉由設定登錄機碼底下的或登錄值，來改變和 countersets 的行為， `Process` `Thread` 以使用唯一的實例名稱 `ProcessNameFormat` `ThreadNameFormat` `HKLM\System\CurrentControlSet\Services\Perfproc\Performance` 。

> [!CAUTION]
> 啟用 counterset 的唯一實例名稱 `Process` 可能會導致某些程式的行為不正確，因為許多程式都預期非唯一的命名模式。 例如，在尋找具有特定知名 EXE 名稱之實例的程式，在啟用唯一的實例名稱之後，將無法再找到該實例。

這些值的登錄類型為 `REG_DWORD` 。 將值設定為會 `2` 附加處理序識別碼 (PID) 至進程實例名稱和執行緒識別碼 (TID) 至執行緒實例名稱。 若要停用此功能，請將值設定為1，或刪除值。
