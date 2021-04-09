---
description: 可轉移元件的一般用途是在系統升級期間準備要重新安裝的產品。
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: 使用可轉移的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35982aafd486a62ce8560e507b8b6caf88e32591
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103945756"
---
# <a name="using-transitive-components"></a>使用可轉移的元件

可轉移元件的一般用途是在系統升級期間準備要重新安裝的產品。 安裝套件的作者會指定在系統升級期間必須交換為具有可轉移屬性的元件。 當使用者稍後升級系統時，必須重新安裝產品。 重新安裝之後，安裝程式會移除先前的元件，並安裝較新的元件，而不需要安裝整個產品。

**在安裝套件中包含兩個可轉移的元件**

1.  在安裝套件中包含這兩個可轉移的元件。
2.  將兩個可轉移的元件撰寫成 [元件資料表](component-table.md) ，與一般元件相同。 每個可轉移的元件都必須在 [元件] 資料行中指定自己的唯一 GUID。
3.  在元件資料表的 [屬性] 資料行中包含每個可轉移元件的 **msidbComponentAttributesTransitive** 位。 如果設定此位，則安裝程式會在重新安裝時重新評估 [條件] 資料行中的語句值。

    如果值先前是 False，且已變更為 True，則安裝程式會安裝元件。

    如果值先前是 True 且已變更為 False，即使元件有其他產品做為用戶端，安裝程式也會移除該元件。

    > [!Note]  
    > 除非已設定可轉移位，否則即使在產品的後續維護安裝中，條件陳述式會評估為 False，仍然會在安裝後啟用元件。 條件必須只以電腦狀態為基礎。 請勿依據命令列上設定的使用者狀態或屬性來使用 with 條件，因為這可能會導致安裝程式要求不同使用者在每次使用時都必須重新安裝產品。

     

4.  在控制資料表的 [條件] 欄位中輸入互補的條件運算式，如此一來，當第一個可轉移元件上的條件變更為 False 時，第二個可轉移元件上的條件會變更為 True。 這會導致在重新安裝應用程式時，移除第一個元件和第二個元件的安裝。

若要切換可轉移的元件，必須重新安裝產品。 因此，封裝作者必須為使用者提供重新安裝產品的方法，以及設定 [**REINSTALLMODE**](reinstallmode.md) 屬性的模式。 基本上，有三種方式可觸發重新安裝：

-   藉由撰寫使用 [*完整 UI*](f-gly.md)的封裝，執行並設定透過使用者介面重新安裝。
-   使用 **msiexec/f** 從命令列執行重新安裝，然後從 [ **/f** [命令列] 選項](command-line-options.md)的清單中選取模式。
-   讓應用程式呼叫 [**MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) 或 [**MsiReInstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)。

此位應僅用於以電腦狀態為基礎的條件。 請勿依據命令列上設定的使用者狀態或屬性來使用 with 條件，因為這可能會導致安裝程式要求不同使用者在每次使用時都必須重新安裝產品。

> [!Note]
> 除非針對元件設定 [屬性] 資料行中的可轉移位，否則即使在 [條件] 資料行中的條件陳述式在產品的後續維護安裝中評估為 False，仍然會在安裝後啟用此元件。
> 
> 在大部分情況下，如果應用程式包含可轉移的元件，Windows Installer 要求應用程式的來源修復或升級應用程式。 在這些情況下，原始設備製造商所附的系統還原 CD-ROM 無法運作，且需要提供應用程式的實際安裝來源。

 

 

 



