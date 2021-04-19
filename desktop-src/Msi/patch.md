---
description: 安裝程式會藉由呼叫 MsiApplyPatch、MsiApplyMultiplePatches 或/p 命令列選項，將 PATCH 屬性設為要套用的修補程式清單。
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: PATCH 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983142"
---
# <a name="patch-property"></a>PATCH 屬性

安裝程式會藉由呼叫 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)、 [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)或/p [命令列選項](command-line-options.md)，將 **PATCH** 屬性設為要套用的修補程式清單。 您也可以在使用 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)或/I 命令列選項安裝封裝時，在命令列上設定 **PATCH** 屬性。

**PATCH** 屬性的值是要安裝的修補程式清單。 清單中的每個修補程式都會以修補程式套件 ( .msp 檔案的完整路徑來表示。 ) 清單中的完整路徑會以分號分隔。

**Windows Installer 2.0：** 不支援多個修補程式。 需要 Windows Installer 3.0 才能套用多個修補程式。

## <a name="remarks"></a>備註

如果您使用 [Msimsp.exe](msimsp-exe.md) 建立修補程式套件，而且 [Patchwiz.dll](patchwiz-dll.md) 可以指定在套用特定修補程式時，只執行一個動作或一個對話方塊。 當您建立修補程式套件時（例如 test .msp），您會撰寫產品的升級映射和修補程式建立屬性檔。 撰寫修補程式建立屬性檔時，您可以在 [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) 資料表的 MediaSrcPropName 欄位中輸入屬性名稱（例如 PATCHFORTEST）。 當您撰寫升級之產品影像的順序資料表時，可以在 sequence 資料表的 [條件] 資料行中，加入您想要進行條件化之動作或對話方塊的條件式語句。

例如，您可以使用下列條件陳述式，只在套用了測試 .msp 時執行動作或對話方塊。

<dl> 修補程式和 PATCHFORTEST 和修補程式 >< PATCHFORTEST  
</dl>

> [!Note]  
> 由於 **PATCH** 屬性可以包含多個修補程式，請使用 substring 運算子 "><" 來測試是否有特定的修補程式，而不是 equals 運算子 "="。 如需條件陳述式的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md) 一節。

 

如果您套用包含 test .msp 的修補程式清單，安裝程式會設定這兩個屬性。 例如，您可以使用/p [命令列選項](command-line-options.md) 來套用兩個修補程式的清單。

**msiexec/qb/p \\ \\ 臨時 \\ 臨時 \\ 臨時 \\ 修補程式 \\ 測試 .msp; \\ \\臨時 \\ \\ 的 XYZ \\ bar .msp**

安裝程式會設定 **PATCH** 和 PATCHFORTEST 屬性，如下所示。

<dl> PATCH = \\ \\ 臨時 \\ 臨時 \\ \\ 的 XYZ 修補程式 \\ 測試 .msp; \\ \\臨時 \\ \\ 的 XYZ \\ bar .msp  
PATCHFORTEST = \\ \\ 臨時 \\ 臨時 \\ \\ 的 XYZ 修補程式 \\ 測試 .msp  
</dl>

在此情況下，條件為 TRUE，而且上述條件式動作或對話方塊可以針對每個所安裝的修補程式、測試 .msp 和 .msp 執行。

如果未套用 .msp，安裝程式就不會將它包含在 **PATCH** 屬性中，也不會設定 PATCHFORTEST。 在此情況下，上述條件為 FALSE，而條件式動作或對話方塊則不會執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[條件陳述式語法](conditional-statement-syntax.md)
</dt> <dt>

[條件陳述式語法的範例](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




