---
description: InstallWiaDevice 函式會將 Windows 映像取得 (WIA) 裝置安裝為根列舉的裝置。 如果有任何安裝的檔案或 coinstaller 未經過數位簽署且受信任，它可能會彈出安全性警告。
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: 'InstallWiaDevice 函式 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691108"
---
# <a name="installwiadevice-function"></a>InstallWiaDevice 函式

**InstallWiaDevice** 函式會將 Windows 映像取得 (WIA) 裝置安裝為根列舉的裝置。 如果有任何安裝的檔案或 coinstaller 未經過數位簽署且受信任，它可能會彈出安全性警告。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWiaDeviceInstall* \[在\]
</dt> <dd>

類型： **PWIADEVICEINSTALL \** _

WIADEVICEINSTALL 結構的指標。 結構的 _szFriendlyName * 成員必須設定為實際的裝置 FriendlyName。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **DWORD**

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則會傳回 Win32 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 




