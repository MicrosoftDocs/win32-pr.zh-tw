---
title: 'SELFLAG 常數 (Oleacc) '
description: 本主題說明用來指定如何選取可存取物件或取得焦點的常數值。
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b4d0384b66919a55d55593d2e16c9a187d84ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478577"
---
# <a name="selflag-constants"></a>SELFLAG 常數

本主題說明用來指定如何選取可存取物件或取得焦點的常數值。 常數定義于 oleacc 中，並與 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) 方法搭配使用。

不允許下列組合：

-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION
-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION

**用戶端注意事項：** Microsoft Active Accessibility 不支援選取 [編輯] 和 [rich edit] 控制項中包含的文字，因為該文字會在物件的 [值] [屬性](value-property.md)中公開為字串。

如需有關如何執行複雜選取作業的詳細資訊，請參閱 [選取子物件](selecting-child-objects.md)。




| 常數/值 | Description | 
|----------------|-------------|
| <span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl><dt><strong>SELFLAG_NONE</strong></dt><dt>0</dt></dl> | 不執行任何動作。 Microsoft Active Accessibility 不會變更選取範圍或焦點。<br /> | 
| <span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl><dt><strong>SELFLAG_TAKEFOCUS</strong></dt><dt>0x1</dt></dl> | 將焦點設定為物件，並使其成為選取錨點。 此旗標本身會使用此旗標來變更選取專案。 其效果類似于手動移動焦點，方法是按住方向鍵，同時按住 CTRL 鍵 Windows 檔案總管或任意多重選取清單方塊中。 <br /> 使用具有 <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>的物件，SELFLAG_TAKEFOCUS 會結合下列值：<br /><ul><li>SELFLAG_TAKESELECTION</li><li>SELFLAG_EXTENDSELECTION</li><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li><li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li></ul>如果您使用具有<strong>HWND</strong>的物件上的 SELFLAG_TAKEFOCUS 旗標來呼叫<a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible：： accSelect</strong></a> ，只有當物件的父系已經有焦點時，旗標才會生效。<br /> | 
| <span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl><dt><strong>SELFLAG_TAKESELECTION</strong></dt><dt>0x2</dt></dl> | 選取物件，並將選取專案從容器中的所有其他物件中移除。 <br /> 除非它與 SELFLAG_TAKEFOCUS 合併，否則此旗標不會變更焦點或選取錨點。 SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS 組合相當於按一下 Windows 檔案總管中的專案。<br /> 此旗標不得與下列旗標結合：<br /><ul><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_EXTENDSELECTION</li></ul> | 
| <span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt><dt>0x4</dt></dl> | 變更選取範圍，讓選取範圍錨點和此物件之間的所有物件都採用錨點物件的選取狀態。 如果不選取錨點物件，物件會從選取項目移除。 如果選取錨點物件，則會擴充選取範圍，以包含此物件和之間的所有物件。 藉由結合此旗標與 SELFLAG_ADDSELECTION 或 SELFLAG_REMOVESELECTION 來設定選取狀態。 <br /> 除非它與 SELFLAG_TAKEFOCUS 合併，否則此旗標不會變更焦點或選取錨點。 SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS 組合相當於以手動方式將專案新增至選取範圍，方法是按住 SHIFT 鍵，然後按一下 Windows 檔案總管中未選取的物件。<br /> 此旗標不會與 SELFLAG_TAKESELECTION 結合。<br /> | 
| <span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl><dt><strong>SELFLAG_ADDSELECTION</strong></dt><dt>0x8</dt></dl> | 將物件加入至目前的選取專案;可能的結果是非連續的選取專案。 <br /> 除非它與 SELFLAG_TAKEFOCUS 合併，否則此旗標不會變更焦點或選取錨點。 SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS 組合相當於以手動方式將專案新增至選取範圍，方法是按住 CTRL 鍵，然後按一下 Windows 檔案總管中未選取的物件。<br /> 此旗標不會與 SELFLAG_REMOVESELECTION 或 SELFLAG_TAKESELECTION 合併。<br /> | 
| <span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl><dt><strong>SELFLAG_REMOVESELECTION</strong></dt><dt>0x10</dt></dl> | 從目前的選取範圍中移除物件;可能的結果是非連續的選取專案。 <br /> 除非它與 SELFLAG_TAKEFOCUS 合併，否則此旗標不會變更焦點或選取錨點。 SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS 組合相當於手動移除選取專案中的專案，方法是按住 CTRL 鍵，同時按一下 Windows 檔案總管中選取的物件。<br /> 此旗標不會與 SELFLAG_ADDSELECTION 或 SELFLAG_TAKESELECTION 合併。<br /> | 




## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Oleacc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[選取子物件](selecting-child-objects.md)
</dt> </dl>

 

 





