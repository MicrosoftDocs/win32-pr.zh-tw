---
description: 確認 DVD 光碟機中的媒體區域與 DVD 光碟機區域相符。
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DvdLauncher 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: a52ac620e5ec9aa3d9060d35921fcfd9c5bcc6e73cebf71ef336ceb54fc0806e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956907"
---
# <a name="dvdlauncher-function"></a>DvdLauncher 函式

確認 DVD 光碟機中的媒體區域與 DVD 光碟機區域相符。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*HWnd* \[在\]
</dt> <dd>

最上層視窗的控制碼，可用於任何必要的使用者介面。

</dd> <dt>

*R* \[在\]
</dt> <dd>

磁碟機號。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函數成功且區域相符，則傳回值為非零值。 否則，傳回值為零。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 StorProp.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                          |
| DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[裝置管理函式](device-management-functions.md)
</dt> </dl>

 

