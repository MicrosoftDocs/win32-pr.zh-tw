---
title: CounterItem Width 屬性
description: 抓取或設定用來繪製計數器值的線條寬度。
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- 寬度屬性 SysMon
- Width 屬性 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，Width 屬性
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685979"
---
# <a name="counteritemwidth-property"></a>CounterItem Width 屬性

抓取或設定用來繪製計數器值的線條寬度。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Property Width As Long
```



## <a name="property-value"></a>屬性值

線條圖形中所使用的線條寬度。 有效值的範圍從1到3，其中 1 (預設值) 是最小寬度。

**在 Windows Vista 之前：** 有效的值範圍從1到9。 如果您的應用程式將會在 Windows Vista 上執行，請勿使用大於3的寬度值。

## <a name="exceptions"></a>例外狀況



| 例外狀況類型               | 條件                              |
|------------------------------|----------------------------------------|
| **System. ArgumentException** | 指定的線條寬度無效。 |



 

## <a name="remarks"></a>備註

您新增的前十六個計數器的預設行寬度為1。 接下來16個計數器的預設行寬度 (您新增的計數器 17-32) ：2。 接下來16個計數器的預設行寬度 (計數器 33-48) 您新增的是3。 之後，SYSMON 會隨機播放線條寬度。 如需詳細資訊，請參閱 [**CounterItem。**](counteritem-color.md)

若要指定純色以外的 [**線條樣式**](counteritem-linestyle.md) ，寬度必須為1。 如果您指定大於1的值，並指定非實線樣式，SYSMON 會忽略指定的線條寬度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





