---
title: " (WSManDisp 的列舉常數) "
description: 列舉包含下列清單所列的常數，會透過呼叫 Session. 列舉和 Iwsmansession.invoke 列舉來用於旗標參數中。
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c8182352d2ebf3763a38f74dd6f100dc836e88cfa10212ffaa971048ebd1aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113260"
---
# <a name="enumeration-constants"></a>列舉常數

**\_ \_ WSManEnumFlags** 列舉包含下列清單中所列的常數，會透過呼叫 [**Session. 列舉**](session-enumerate.md)和 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)來用於 *旗標* 參數中。

請注意，如果未指定 *flags* 參數， **WSManFlagReturnObject** 和 **WSManFlagHierarchyDeep** 是預設值。

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**
</dt> <dd> <dl> <dt>

0 (0x0) 
</dt> <dt>



批次包含要求的 XML 實例。 這是旗標參數的預設值。

相關聯的腳本方法是 [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



此旗標會控制對 Session 呼叫中 *篩選* 參數的方式。由 WinRM 來解讀 [**列舉**](session-enumerate.md) 。

篩選的格式可以是 XML 片段或純文字字串。 格式取決於呼叫 [**Session. 列舉**](session-enumerate.md)或 [**Iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)中所使用之 [*篩選*](windows-remote-management-glossary.md)條件的 [*篩選方言*](windows-remote-management-glossary.md)。

如果未指定 *方言* 參數，WinRM 會嘗試根據篩選準則的第一個字元來決定方言。 如果 < 第一個字元，但篩選並不是 XML 片段，則應該設定此旗標。 例如，下列格式的篩選準則需要您設定 **WSManFlagNonXmlText** ，才能正確地解讀篩選：

`<25 && > 1`

如果篩選是 XML 片段，則不需要此旗標，因為片段會以 < （WinRM 正確地解讀為 XML）開頭。 例如

`<filter>select * from aDataStructure</filter>`

如果篩選是不是以 < 開頭的純文字，則不需要此旗標。 例如

`select * from aDataStructure`

相關聯的腳本方法是 [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext)。


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**
</dt> <dd> <dl> <dt>

2 (0x2) 
</dt> <dt>



批次包含對應 XML 實例 (EPRs) 的端點參考，但不包含實際實例。

相關聯的腳本方法是 [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**
</dt> <dd> <dl> <dt>

4 (0x4) 
</dt> <dt>



批次包含所要求的 XML 實例，以及 [*wsman： Items*](windows-remote-management-glossary.md) 元素中包含的對應 EPRs。

相關聯的腳本方法是 [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**
</dt> <dd> <dl> <dt>

0 (0x0) 
</dt> <dt>



系統會包含衍生類別實例，並根據其實際的架構來表示。

相關聯的腳本方法是 [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**
</dt> <dd> <dl> <dt>

32 (0x20) 
</dt> <dt>



排除衍生類別實例。 只會顯示所要求之類型的實例。

相關聯的腳本方法是 [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow)。


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**
</dt> <dd> <dl> <dt>

64 (0x40) 
</dt> <dt>



系統會包含衍生類別實例，並根據基類架構來表示。 不會顯示衍生類別中定義的屬性。

相關聯的腳本方法是 [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly)。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WinRM 常數和列舉](winrm-constants-and-enumerations.md)
</dt> <dt>

[列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[查詢資源的特定實例](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





