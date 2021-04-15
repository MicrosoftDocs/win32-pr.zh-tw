---
description: SetDelayTime 方法會設定與 MSWebDVD 物件相關聯的工具提示延遲時間。
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467408"
---
# <a name="setdelaytime"></a>SetDelayTime

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`SetDelayTime`方法會設定與 **MSWebDVD** 物件相關聯的工具提示延遲時間。

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*
</dt> <dd>

將延遲的類型指定為整數。



| 值 | 描述                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -1    | 若要將 autopop 延遲時間重設為預設值，請將 *iNewVal* 設定為-1。                                                                                                                                                                       |
| 0     | 設定當指標在工具周框內為固定時，工具提示視窗保持可見的時間長度。                                                                                                                         |
| 1     | 設定在顯示工具提示視窗之前，指標必須保持在工具周框內保持靜止的時間長度。                                                                                                                    |
| 2     | 設定當指標從某個工具移至另一個工具時，後續工具提示視窗顯示所需的時間長度。                                                                                                                          |
| 3     | 將所有延遲時間設定為預設比例。 Autopop 時間是初始時間的10倍，而 reshow 時間是初始時間的一到五倍。 如果設定此旗標，請使用正值 iNewVal 來指定初始時間（以毫秒為單位）。 |



 

</dd> <dt>

<span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*
</dt> <dd>

指定以毫秒為單位的延遲（以毫秒為單位）。



| 值                    | 描述                                                   |
|--------------------------|---------------------------------------------------------------|
| -1                       | 將 *iDelayType* 中指定的延遲設定為其預設值 |
| 任何其他負數值 | 將所有延遲類型設定為其預設值。                  |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

 

 



