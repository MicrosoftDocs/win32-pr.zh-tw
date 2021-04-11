---
description: 設定電腦監視器的顯示亮度。
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: WmiMonitorBrightnessMethods 類別的 WmiSetBrightness 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026965"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>WmiMonitorBrightnessMethods 類別的 WmiSetBrightness 方法

**WmiSetBrightness** 方法會設定電腦監視器的顯示亮度。

## <a name="syntax"></a>語法


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*逾時* 
</dt> <dd>

Timeout （以秒為單位）。

</dd> <dt>

*亮度* 
</dt> <dd>

亮度（以百分比表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。

## <a name="examples"></a>範例

如需有關如何抓取及設定監視器亮度的詳細討論，請參閱「腳本撰寫者 [使用 PowerShell 來報告和設定監視器亮度](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) 的 blog」主題。

下列 PowerShell 範例會將監視的亮度設定為50%。


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

