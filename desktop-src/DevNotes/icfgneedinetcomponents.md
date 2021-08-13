---
description: 判斷在選項中標示的元件是否已安裝在系統上。
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: IcfgNeedInetComponents 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 9b0d533e234986f54c6a4de668273bda08d9c810dc9f5a93acb3aaf030cea665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390658"
---
# <a name="icfgneedinetcomponents-function"></a>IcfgNeedInetComponents 函式

判斷在選項中標示的元件是否已安裝在系統上。

## <a name="syntax"></a>語法


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwfOptions* 
</dt> <dd>

下列旗標的組合，可指定要從下列清單中偵測哪些元件。



| 值                                                                                                                                                                                                                                  | 意義                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_INSTALLMAIL**</dt> <dt>0x00000004</dt> </dl> | 需要 Exchange 或網際網路郵件？<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | 需要 RAS 嗎？<br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | 是否需要 TCP/IP？<br/>                    |



 

</dd> <dt>

*lpfNeedComponents* 
</dt> <dd>

如果這個值不是 **Null**，則如果系統上未安裝一或多個元件，則會傳回 **TRUE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 如果沒有發生錯誤，則會傳回 **錯誤 \_ 成功** 碼。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
