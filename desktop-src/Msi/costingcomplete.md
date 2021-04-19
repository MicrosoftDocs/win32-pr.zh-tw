---
description: CostingComplete 屬性會指出安裝程式是否已完成磁碟空間的成本。
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: CostingComplete 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995689"
---
# <a name="costingcomplete-property"></a>CostingComplete 屬性

**CostingComplete** 屬性會指出安裝程式是否已完成磁碟空間的成本。 如果尚未完成成本計算，這個屬性可用來撰寫觸發的對話方塊。 此屬性會在磁碟空間成本設定期間動態設定，並在完成成本設定時立即設定為1。 [CostFinalize 動作](costfinalize-action.md)會將這個屬性初始化為0。

## <a name="remarks"></a>備註

如需如何撰寫「請稍候」的範例。 . . "在磁碟空間成本中快顯的對話方塊中，請參閱 [撰寫條件式「請稍候 ...」一節。訊息方塊](authoring-a-conditional-please-wait-------message-box.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




