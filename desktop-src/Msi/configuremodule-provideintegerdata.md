---
description: Mergemod.dll 會呼叫 ConfigureModule 物件的 ProvideIntegerData 方法，以從用戶端工具中取出整數資料。
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: 'ConfigureModule. ProvideIntegerData 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981399"
---
# <a name="configuremoduleprovideintegerdata-method"></a>ConfigureModule. ProvideIntegerData 方法

Mergemod.dll 會呼叫 [**ConfigureModule 物件**](configuremodule-object.md)的 **ProvideIntegerData** 方法，以從用戶端工具中取出整數資料。

Mergemod.dll 從 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中的對應專案提供 *名稱*。

此工具應該會傳回 \_ [確定]，並在 *ConfigData* 中提供適當的自訂整數。

如果工具未提供任何此 *名稱* 值的設定資料，此函式應該會傳回 \_ FALSE。 在此情況下 Mergemod.dll 會忽略 *ConfigData* 引數的值，並使用 ModuleConfiguration 資料表中的預設值。

## <a name="syntax"></a>語法


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* 
</dt> <dd>

要抓取資料的專案名稱。

</dd> <dt>

*ConfigData* 
</dt> <dd>

自訂文字的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

針對 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中的每一筆記錄，用戶端可能只會被呼叫一次。 請注意，Mergemod.dll 永遠不會對相同的「名稱」值進行多個用戶端呼叫。 如果 ModuleSubstitution 資料表中沒有任何記錄使用屬性，ModuleConfiguration 資料表中的專案就不會呼叫用戶端。

### <a name="c"></a>C++

請參閱 [**ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata)函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 2.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




