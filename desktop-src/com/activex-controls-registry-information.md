---
title: ActiveX控制登錄資訊
description: ActiveX控制登錄資訊
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f062c11304c50161308cc5c6e43001c23f63486e60e568f61d6335f0947380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737382"
---
# <a name="activex-controls-registry-information"></a>ActiveX控制登錄資訊

有一些登錄專案和旗標會使用。 此外，控制項可以支援元件類別，以分類它們所提供的功能。

與控制項相關的登錄機碼會在下列樹狀結構中標示為星號：

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

**DefaultIcon** 專案是用來識別將控制項最小化至圖示時所要顯示的圖示。 [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona)函式是用來從指定的 .DLL 或 .EXE 檔案取得圖示。

**ToolboxBitmap32** 專案會識別 \* 要用於工具列或工具箱按鈕臉部的 16 15 點陣圖的模組名稱和資源識別碼。 標準 Windows 圖示大小太大，無法用於此用途。 此專案特別支援控制項容器，這些容器具有設計模式，其中一個會選取控制項，並將其放在設計的表單上。 例如，在 Visual Basic 中，控制項的圖示會在設計模式期間顯示于 Visual Basic 工具箱中。

**控制項** 專案會將物件標示為控制項。 容器通常會使用此專案來填滿對話方塊。 容器會使用這個子機碼來判斷是否要在顯示控制項的對話方塊中包含物件。

可 **插入** 的子索引鍵也可以與控制項搭配使用，這取決於物件是否只能做為就地内嵌物件，且沒有特殊的控制項功能。 標記為 [插入] 的 **物件會顯示** 在其容器的 [插入物件] 對話方塊中。 可 **插入** 的專案通常表示控制項已經過非控制項容器的測試。

可 **插入** 和 **控制** 子機碼都是選擇性的。 如果控制項不是設計來使用不了解控制項的舊容器，則可以省略可 **插入** 的子機碼。 如果控制項的設計目的是要使用特定的容器，而不想要插入其他容器中，則控制項可以省略該 **控制項** 索引鍵。

控制項應該有屬性動詞、OLEIVERB \_ 屬性，以及它們所支援的任何其他動詞。 Properties 動詞以及標準動詞 OLEIVERB \_ PRIMARY，會指示控制項顯示其屬性工作表。 當控制項為使用中時，[屬性] 動詞會顯示為容器功能表上的 [屬性] 專案。 如此一來，控制項可以顯示自己的屬性頁，讓使用者有一些實用的功能，即使容器不會處理控制項。

控制項會定義 **MiscStatus** 索引鍵，以描述其本身至可能的容器。 Bits 會採用 [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)的值，而控制項會將數個值新增至此列舉。 如需詳細資訊，請參閱 **OLEMISC** 列舉值。 用戶端可以呼叫 [**IOleObject：： GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) 來取得這項資訊，而不需要先將控制項具現化。

最後， **version** 描述的控制項版本應符合與此控制項相關聯之類型程式庫的版本。

此外，在控制項的類型資訊中，屬性控制項會將 coclass 專案標記為描述控制項。

 

 