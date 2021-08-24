---
description: 若為安裝套件，[範本摘要] 屬性會指出與此安裝資料庫相容的平臺和語言版本。
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: 範本摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da93d2d3a38f3c1853f3f936fe6f97b8550dcaeac70d4b553b8cb0362f41ee41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893448"
---
# <a name="template-summary-property"></a>範本摘要屬性

若為安裝套件，[ **範本摘要** ] 屬性會指出與此安裝資料庫相容的平臺和語言版本。 安裝資料庫之 **範本摘要** 屬性資訊的語法如下：

\[*platform 屬性* \] ; \[*語言識別項* \] \[ ，,...*語言識別項* \] \[ \] 。

下列範例是 **範本摘要** 屬性的有效值：

-   x64; 1033
-   Intel; 1033
-   Intel64; 1033
-   ; 1033
-   Intel、1033、2046
-   Intel64; 1033，2046
-   Intel; 0
-   Arm; 1033、2046
-   Arm; 0
-   Arm64; 1033，2046
-   Arm64; 0

轉換的 [ **範本摘要** ] 屬性會指出與轉換相容的平臺和語言版本。 在轉換檔中，只能指定一種語言。 指定的平臺和語言會決定是否可以將轉換套用至特定的資料庫。 如果沒有任何轉換限制依賴它們來驗證轉換，則 platform 屬性和 language 屬性可以保留空白。

Patch 封裝的 [ **範本摘要** ] 屬性是可接受修補程式的產品代碼清單（以分號分隔）。 如果您使用 [Msimsp.exe](msimsp-exe.md) 並 [Patchwiz.dll](patchwiz-dll.md) 來產生修補程式套件，則會從 Patch 建立檔案的 [TargetImages 資料表](targetimages-table-patchwiz-dll-.md) 中取得此清單。

這是必要的摘要屬性。

## <a name="remarks"></a>備註

如果目前的平臺不符合 **範本摘要** 屬性中所指定的其中一個平臺，安裝程式就不會處理封裝。

如果 **範本摘要** 屬性值中缺少平臺規格，則安裝程式會假設採用 Intel 架構。

如果這是在 Intel64 (Itanium) 平臺上執行的64位 Windows Installer 套件，請在 [**範本摘要**] 屬性中輸入 Intel64。

如果這是在 x64 平臺上執行的64位 Windows Installer 套件，請在 [**範本摘要**] 屬性中輸入 x64。

如果這是在 Arm64 平臺上執行的64位 Windows Installer 套件，請在 [**範本摘要**] 屬性中輸入 Arm64。

Windows Installer 套件不可標示為支援 Intel64 和 x64;例如，Intel64，x64 的 **範本摘要** 屬性值無效。

Windows Installer 套件不可標示為支援32位和64位平臺;例如，例如 Intel、x64 或 Intel、Intel64 等 **範本摘要** 屬性值無效。

在 [ **範本摘要** ] 屬性的 [語言識別項] 欄位中輸入 0 (零) ，或將這個欄位保留空白，表示封裝為非語言相關。

如果這是在 Windows RT 上執行 Windows Installer 套件，請在 [**範本摘要**] 屬性中輸入 Arm 的值。

合併模組是唯一可能具有多個語言的封裝。 來源安裝程式資料庫中只能指定一種語言。 如需詳細資訊，請參閱 [多個語言合併模組](multiple-language-merge-modules.md)。

Windows Installer 不支援 Alpha 平臺。

**Windows Installer：** 不支援下列語法：

\[*platform 屬性* \] \[ 、*platform 屬性* \] \[ \] ,... \[*語言識別項* \] \[ ，,...*語言識別項* \] \[ \] 。

下列範例不是 **範本摘要** 屬性的有效值：

-   Alpha、Intel、1033
-   Intel、Alpha、1033
-   Alpha; 1033
-   Alpha、1033、2046

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[摘要屬性描述](summary-property-descriptions.md)
</dt> </dl>

 

 




