---
description: GetGPRM 方法會抓取指定的一般參數 register。
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: GetGPRM 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510239"
---
# <a name="getgprm-method"></a>GetGPRM 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

方法會抓取 `GetGPRM` 指定的一般參數暫存器。

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

指定要取出為整數的暫存器。 值的範圍必須介於0到15之間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數值，代表指定的暫存器。

## <a name="remarks"></a>備註

使用 **MSWebDVD** 物件的 DVD 流覽或播放功能不需要這個方法。 這項功能的目的是為了讓您徹底瞭解想要執行 advanced 功能的 DVD 規格。 GPRMs 可以用來保存任何值，因此可以自由設定和讀取。 但由於 GPRMs 也用來儲存光碟命令，因此使用 [**SetGPRM**](setgprm-method.md) 變更其值可能會導致無法預期的行為。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



