---
description: DVDTimeCode2bstr 方法會抓取表示光碟上目前時間的字串。
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: DVDTimeCode2bstr 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106986228"
---
# <a name="dvdtimecode2bstr-method"></a>DVDTimeCode2bstr 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

方法會抓取 `DVDTimeCode2bstr` 表示光碟上目前時間的字串。

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*
</dt> <dd>

指定光碟上的目前時間，其相對於標題開頭為透過 [**EC \_ DVD \_ 目前 \_ HMSF \_ 時間**](ec-dvd-current-hmsf-time.md) 事件取得的數位。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回11個字元的字串，格式為 "hh： mm： ss： ff"，代表定義目前時間的時、分、秒和框架。

## <a name="remarks"></a>備註

這個方法是唯讀的。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[處理 DVD 事件通知](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



