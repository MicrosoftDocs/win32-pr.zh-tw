---
description: 因為自訂動作可在 UI 和執行順序資料表中排程，而且可以在服務或用戶端進程中執行，所以自訂動作可能會執行多次。
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: 自訂動作執行排程選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986981"
---
# <a name="custom-action-execution-scheduling-options"></a>自訂動作執行排程選項

因為自訂動作可在 UI 和執行順序資料表中排程，而且可以在服務或用戶端進程中執行，所以自訂動作可能會執行多次。

請注意，安裝程式：

-   預設會立即在順序資料表中執行動作。
-   如果 sequence 資料表的條件運算式欄位評估為 False，則不會執行動作。
-   如果內部使用者的介面層級設定為完整的 UI 模式，則處理用戶端進程中的 UI 順序資料表 (如需) 的 UI 層級描述，請參閱 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) 。
-   是使用 Windows 2000 時預設註冊的服務，在此情況下，會在安裝程式服務中處理執行順序資料表。

您可以使用下列選項旗標來控制多個立即執行自訂動作。 若要設定選項，請將此資料表中的值加入至 [CustomAction 資料表](customaction-table.md)之 [類型] 欄位中的值。 下列旗標都不應搭配延後 [執行自訂動作](deferred-execution-custom-actions.md)使用。

<dl> <dt>

<span id="_default_"></span><span id="_DEFAULT_"></span> (預設) 
</dt> <dd>

十六進位：0x00000000

Decimal：0

一律執行。 如果兩個順序資料表中都有動作，動作可能會執行兩次。

</dd> <dt>

<span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence** 
</dt> <dd>

十六進位：0x00000100

Decimal：256

如果同時存在於兩個順序資料表中，則不會執行一次以上。 如果 UI 順序已執行，一律會略過執行順序中的動作。 UI 順序中沒有任何作用。 動作不一定要存在，也不能在 UI 順序中執行，以在執行順序中略過。 不受安裝服務註冊的影響。

</dd> <dt>

<span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**
</dt> <dd>

十六進位：0x00000200

Decimal：512

如果在這兩個順序資料表中，每個進程執行一次。 如果 UI 序列已在相同的進程中執行，例如在用戶端進程中執行，則會略過執行序列中的動作。 用來防止修改會話狀態的動作，例如屬性和資料庫資料，而不是執行兩次。

</dd> <dt>

<span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**
</dt> <dd>

十六進位：0x00000300

Decimal：768

只有在 UI 循序執行後於用戶端上執行時才執行。 只有當執行順序是在用戶端上執行的執行順序之後，才會執行動作。 可以用來提供或邏輯，或隱藏 UI 相關的處理（如果用戶端會話已完成）。

</dd> </dl>

請注意，若要在兩個不同的執行模式中執行自訂動作，請在 [CustomAction 資料表](customaction-table.md) 中撰寫兩個專案。 例如，若要讓自訂動作呼叫 C/c + + 動態連結程式庫 (DLL)  ( [自訂動作類型 1](custom-action-type-1.md)) 當模式 MSIRUNMODE \_ 排程和 MSIRUNMODE 回復時 \_ ，請將兩個專案放在呼叫相同 DLL 但具有不同數數值型別的 CustomAction 資料表中。 包含呼叫 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 的程式碼，以判斷何時要執行哪個自訂動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂動作參考](custom-action-reference.md)
</dt> <dt>

[關於自訂動作](about-custom-actions.md)
</dt> <dt>

[使用自訂動作](using-custom-actions.md)
</dt> </dl>

 

 



