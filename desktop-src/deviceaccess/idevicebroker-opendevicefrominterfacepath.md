---
title: IDeviceBroker OpenDeviceFromInterfacePath 方法
description: 嘗試代表用戶端開啟裝置介面實例。 IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98。
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- OpenDeviceFromInterfacePath 方法 Device Access Broker API
- OpenDeviceFromInterfacePath 方法 Device Access Broker API，IDeviceBroker 介面
- IDeviceBroker 介面裝置存取代理程式 API，OpenDeviceFromInterfacePath 方法
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374338"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>IDeviceBroker：： OpenDeviceFromInterfacePath 方法

> [!Important]  
> 這些介面不受支援，且不應該使用。 請改用 [裝置存取 API c + + 程式設計參考](device-access-api-c---programming-reference.md) 中的 api。

嘗試代表用戶端開啟裝置介面實例。 IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98。

## <a name="syntax"></a>語法

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*pszDeviceInterfacePath* \[在\]
</dt> <dd>

要開啟的裝置介面實例。

</dd> <dt>

*desiredAccess* \[在\]
</dt> <dd>

要傳遞至 open 的預期存取權。

</dd> <dt>

*shareMode* \[在\]
</dt> <dd>

要傳遞至 open 的共用模式。

</dd> <dt>

*flagsAndAttributes* \[在\]
</dt> <dd>

要傳遞至 open 的旗標和屬性。

</dd> <dt>

*\* phDevice* \[\]
</dt> <dd>

開啟成功時產生的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，它會傳回 S_OK。 否則，它會傳回 HRESULT 錯誤碼。
