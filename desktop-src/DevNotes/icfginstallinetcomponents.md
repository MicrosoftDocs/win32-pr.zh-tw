---
description: 安裝指定的系統元件。
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: IcfgInstallInetComponents 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 7708dd065c066ce3e9fd8e4de1044c6bc8587d2526abdf9aeac175b4387dec42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827220"
---
# <a name="icfginstallinetcomponents-function"></a>IcfgInstallInetComponents 函式

安裝指定的系統元件。

## <a name="syntax"></a>語法


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* 
</dt> <dd>

父視窗的控制碼。

</dd> <dt>

*dwfOptions* 
</dt> <dd>

下列旗標的組合，可控制安裝和設定。



| 值                                                                                                                                                                                                                                  | 意義                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_INSTALLMAIL**</dt> <dt>0x00000004</dt> </dl> | 安裝 Exchange 與網際網路郵件。<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | 如有需要，請安裝 RAS () 。<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | 如有需要，請將 TCP/IP (安裝) 。<br/>         |



 

</dd> <dt>

*lpfNeedsRestart* 
</dt> <dd>

如果這個值不是 **Null**，則在傳回時，只有在必須重新開機 Windows 才能完成安裝時，才會傳回 **TRUE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 如果沒有發生錯誤，則會傳回 **錯誤 \_ 成功** 碼。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
