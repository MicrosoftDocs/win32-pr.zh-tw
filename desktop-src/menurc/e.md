---
title: 'E (功能表和其他資源) '
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093700"
---
# <a name="e-menus-and-other-resources"></a>E (功能表和其他資源) 

[](a.md) [B](b.md) [C](c.md) D [](u.md) [](v.md) E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**不允許空白功能表**
</dt> <dd>

在 [**功能表**](menu-resource.md)語句中定義任何功能表項目之前，會出現 **END** 關鍵字。 Microsoft Windows 32 資源編譯器 (RC) 不允許空的功能表。 請確定 **功能表** 語句內沒有任何左引號。

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**對話方塊中預期的結尾**
</dt> <dd>

**End** 關鍵字必須出現在 [**DIALOG**](dialog-resource.md)語句的結尾。 請確定前面的語句沒有任何左引號。

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**功能表中的預期結尾**
</dt> <dd>

**End** 關鍵字必須出現在 [**功能表**](menu-resource.md)語句的結尾。 請確定沒有不相符的 **BEGIN** 和 **END** 語句。

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**錯誤 Creatingresource-名稱**
</dt> <dd>

Microsoft Windows 32 資源編譯器 (RC) 無法建立指定的二進位資源 (。RES) 檔。 請確定它不是在唯讀磁片磁碟機上建立的。 您可以使用 **/v** 選項來找出檔案是否正在建立。

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**快速鍵對應表中應有逗號**
</dt> <dd>

Microsoft Windows 32 資源編譯器 (RC) 需要 [**快速鍵**](accelerators-resource.md)語句中的 *事件* 和 *idvalue* 參數之間必須有逗號。

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**預期的控制項類別名稱**
</dt> <dd>

[**對話方塊**](dialog-resource.md)語句中 [**control**](control-control.md)語句的 *class* 參數必須是下列其中一個控制項類型：**按鈕**、 [**COMBOBOX**](combobox-control.md)、**編輯**、 [**LISTBOX**](listbox-control.md)、[**捲軸**](scrollbar-control.md)、**靜態** 或使用者定義。 請確定類別拼寫正確。

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**預期的字型名稱**
</dt> <dd>

[**對話方塊**](dialog-resource.md)語句中 FONT 語句的 **font-size** *參數必須* 是以雙引號括住的字元字串 ( ") 。 此參數會指定字型的名稱。

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Menuitem 的預期識別碼值**
</dt> <dd>

[**MENU**](menu-resource.md)語句必須包含 [**MENUITEM**](menuitem-statement.md)語句，此語句在 *MenuID* 參數中有整數或符號常數。

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**預期的功能表字串**
</dt> <dd>

每個 [**MENUITEM**](menuitem-statement.md) 和 [**POPUP**](popup-resource.md) 語句都必須包含 *文字* 參數。 這個參數是以雙引號括住的字串 ( ") ，可指定功能表項目或快顯功能表的名稱。 **MENUITEM 分隔符號** 語句不需要加上引號的字串。

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**預期的數值命令值**
</dt> <dd>

Microsoft Windows 資源編譯器 (RC) 在 [**快速鍵**](accelerators-resource.md)語句中必須要有數值 *idvalue* 參數。 請確定您已使用 [**\# define**](-define.md)語句來指定值，而且使用的常數拼寫正確。

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**字串資料表中應有數值常數**
</dt> <dd>

定義在 [**\# 定義**](-define.md)語句中的數值常數，必須緊接在 [**STRINGTABLE**](stringtable-resource.md)語句中的 **BEGIN** 關鍵字後面。

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**預期的數值點大小**
</dt> <dd>

[**對話方塊**](dialog-resource.md)語句中 [**FONT**](font-statement.md)語句的 *dialog* 參數必須是整數點大小值。

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**預期的數值對話常數**
</dt> <dd>

[**對話方塊**](dialog-resource.md)語句需要 *x*、 *y*、*寬度* 和 *高度* 參數的整數值。 請確定這些值（這些值包含在 **對話方塊** 關鍵字之後）不是負數。

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**STRINGTABLE 中的預期字串**
</dt> <dd>

在 [**STRINGTABLE**](stringtable-resource.md)語句中的每個數值 *stringid 指定* 參數之後，預期會有一個字串。

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**預期的字串或常數快速鍵命令**
</dt> <dd>

Microsoft Windows 資源編譯器 (RC) 無法判斷為加速器設定的金鑰。 [**快速鍵**](accelerators-resource.md)語句中的 *事件* 參數可能無效。

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**預期的 VALUE、BLOCK 或 END 關鍵字。**
</dt> <dd>

[**VERSIONINFO**](versioninfo-resource.md)結構需要 **VALUE**、 **BLOCK** 或 **END** 關鍵字。

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**預期的識別碼數目**
</dt> <dd>

在 [**DIALOG**](dialog-resource.md)語句中， [**CONTROL**](control-control.md)語句的 *id* 參數必須是數位。 請確定您有控制項識別碼的數位或 [**\# 定義**](-define.md)語句。

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**需要以引號括住的索引鍵字串**
</dt> <dd>

在 **區塊** 或 **值** 關鍵字之後的索引鍵字串應以雙引號括住。

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**在對話方塊類別中需要引號字串**
</dt> <dd>

在 [**對話方塊**](dialog-resource.md)語句中， [**class**](class-statement.md)語句的 *class* 參數必須是以雙引號括住的整數或字串 ( ") 。

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**需要在對話方塊標題中加上引號的字串**
</dt> <dd>

在 [**對話方塊**](dialog-resource.md)語句中， [**CAPTION**](caption-statement.md)語句的 *captioNtext* 參數必須是字元字串，以雙引號括住 ( ") 。

</dd> </dl>

 

 




