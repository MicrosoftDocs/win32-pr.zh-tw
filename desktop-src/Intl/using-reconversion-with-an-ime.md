---
description: IME 會執行一個稱為 &0034 的功能 \# ; 將&\# 0034;。
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: 搭配 IME 使用漢字重組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5a0453b6ac94da805e00639d2a7a56fd79deca4027d23d47e33aab93e4009b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146841"
---
# <a name="using-reconversion-with-an-ime"></a>搭配 IME 使用漢字重組

IME 會執行稱為「漢字重組」的功能。 一般而言，IMM 只會根據使用者輸入的專案來判斷候選清單。 [重設] 可讓 IMM 根據內容)  (包含的句子，判斷一或多個候選項目。 定義的重組類型很簡單、正常且增強。

當使用者在檔中注意到組合錯誤時，「重做」會很有用。 使用者可以選取該錯誤，然後從功能表中選擇 [重組]。 IME 會使用內容來判斷最佳的取代。 應用程式可以使用 [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) 來支援重組。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用輸入方法管理員](using-input-method-manager.md)
</dt> </dl>

 

 



