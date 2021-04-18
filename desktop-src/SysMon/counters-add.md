---
title: 計數器。 Add 方法
description: 將 CounterItem 實例加入至集合。
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- 新增方法 SysMon
- Add 方法 SysMon，計數器類別
- 計數器類別 SysMon，Add 方法
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464716"
---
# <a name="countersadd-method"></a>計數器。 Add 方法

將 [**CounterItem**](counteritem.md) 實例加入至集合。

## <a name="syntax"></a>語法


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑名稱* \[在\]
</dt> <dd>

計數器的路徑。 路徑可以包含電腦名稱稱，且必須包含效能物件名稱、物件實例名稱（如果指定的效能物件支援多個實例）和計數器名稱。 此路徑規格不區分大小寫。

如需指定計數器路徑的詳細資訊，請參閱 [指定計數器路徑](/windows/desktop/PerfCtrs/specifying-a-counter-path)。

</dd> </dl>

## <a name="exceptions"></a>例外狀況



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>例外狀況類型</th>
<th>條件</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System.runtime.interopservices.outattribute. COMException</strong></td>
<td>您可能會因為下列其中一個原因而收到此例外狀況：
<ul>
<li>在電腦上找不到指定的效能物件。 Err 值為0xC0000BB8。</li>
<li>找不到指定的計數器。 Err 值為0xC0000BB9。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

如果您在 *pathname* 參數中指定萬用字元計數器， **Add** 方法會為每個展開的路徑建立一個 [**CounterItem**](counteritem.md) 物件。 然後， **Add** 方法會傳回第一個加入之 **CounterItem** 的指標。

如果萬用字元會產生重複的計數器，就不會報告錯誤，也不會建立重複的結果。 如果在建立所有計數器之前發生錯誤狀況，則會報告錯誤，並不會建立剩餘的計數器。

您可以新增的計數器數目沒有任何限制;不過，SYSMON 只會圖表集合中的第一個1024計數器。 SYSMON 將在報表中顯示的計數器數目沒有任何限制。

若要在加入計數器時接收通知，請執行 [OnCounterAdded](systemmonitor-oncounteradded.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**計數器**](counters.md)
</dt> <dt>

[**SystemMonitor.BrowseCounters**](systemmonitor-browsecounters.md)
</dt> </dl>

 

