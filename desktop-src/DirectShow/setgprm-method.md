---
description: SetGPRM 方法會將指定的一般參數暫存器設定為指定的值。
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: SetGPRM 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c217f0235ca5b055e20102f553e9e23f5b93e6dd9c3d74db560584690a669ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078858"
---
# <a name="setgprm-method"></a>SetGPRM 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`SetGPRM`方法會將指定的一般參數暫存器設定為指定的值。

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

指定要設定為整數的一般參數暫存器。 整數值的範圍必須介於0到15之間。

</dd> <dt>

<span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*N 值*
</dt> <dd>

將註冊的新值指定為整數。

</dd> </dl>

## <a name="remarks"></a>備註

一般參數暫存器（或 GPRMs）是16位的暫存器，每個光碟都能以獨特的方式用於暫存資料儲存。 播放機應用程式不需要使用 **MSWebDVD** 物件來存取任何標準播放或導覽控制項的這些暫存器。 這種方法是針對執行 advanced 功能的播放程式應用程式所提供。 除非您已徹底瞭解 DVD 規格，以及在播放特定光碟上使用 GPRMs 的方式，否則請勿嘗試直接修改 GPRMs。 變更這些值可能會導致無法預期的行為。

 

 



