---
title: IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread 方法
description: 此 API 會判斷目前內容的權杖是否可存取指定的裝置介面類別別。 IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B。
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- DeviceInterfaceClassAccessCheckWithCallingThread 方法 Device Access Broker API
- DeviceInterfaceClassAccessCheckWithCallingThread 方法 Device Access Broker API，IDeviceAccessPolicyCheck 介面
- IDeviceAccessPolicyCheck 介面裝置存取代理程式 API，DeviceInterfaceClassAccessCheckWithCallingThread 方法
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f279972c3b716f111fa37fc2dd01ef9184b2f804f07106f6b971358daf290c44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635348"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>IDeviceAccessPolicyCheck：:D eviceInterfaceClassAccessCheckWithCallingThread 方法

> [!Important]  
> 這些介面不受支援，且不應該使用。 請改用 [裝置存取 API c + + 程式設計參考](device-access-api-c---programming-reference.md) 中的 api。

此 API 會判斷目前內容的權杖是否可存取指定的裝置介面類別別。 IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B。

## <a name="syntax"></a>語法

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*pszDeviceInterfaceClassGuid* \[在\]
</dt> <dd>

應檢查其存取權的裝置介面類別別 GUID。

</dd> <dt>

*dwClientThreadId* \[在\]
</dt> <dd>

用戶端執行緒識別碼，視需要顯示任何相關聯的 UI。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，它會傳回 S_OK。 否則，它會傳回 HRESULT 錯誤碼。
