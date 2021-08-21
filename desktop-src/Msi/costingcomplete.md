---
description: CostingComplete 屬性會指出安裝程式是否已完成磁碟空間的成本。
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: CostingComplete 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a512621e187be9897c07106ade8c6012d4ac4fa43543d71cb856e90027d549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948355"
---
# <a name="costingcomplete-property"></a>CostingComplete 屬性

**CostingComplete** 屬性會指出安裝程式是否已完成磁碟空間的成本。 如果尚未完成成本計算，這個屬性可用來撰寫觸發的對話方塊。 此屬性會在磁碟空間成本設定期間動態設定，並在完成成本設定時立即設定為1。 [CostFinalize 動作](costfinalize-action.md)會將這個屬性初始化為0。

## <a name="remarks"></a>備註

如需如何撰寫「請稍候」的範例。 . . "在磁碟空間成本中快顯的對話方塊中，請參閱 [撰寫條件式「請稍候 ...」一節。訊息方塊](authoring-a-conditional-please-wait-------message-box.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




