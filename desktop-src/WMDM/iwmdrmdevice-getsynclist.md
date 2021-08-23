---
title: IWMDRMDevice GetSyncList 方法
description: GetSyncList 方法會抓取裝置上的授權同步處理清單。 授權同步處理可讓主機電腦根據指定的準則，將更新的授權傳送至裝置。
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- GetSyncList 方法 windows Media 裝置管理員
- GetSyncList 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetSyncList 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6424daa720f9987228175a7698a29f7056e5d4b4d174d1d635bbcd1ed7f8382
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619578"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>IWMDRMDevice：： GetSyncList 方法

**GetSyncList** 方法會抓取裝置上的授權同步處理清單。 授權同步處理可讓主機電腦根據指定的準則，將更新的授權傳送至裝置。

## <a name="syntax"></a>語法


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cMinCountThreshold* \[在\]
</dt> <dd>

最小計數閾值。

</dd> <dt>

*cMinHoursThreshold* \[在\]
</dt> <dd>

最小時間閾值。

</dd> <dt>

*ppbSyncList* \[擴展\]
</dt> <dd>

已取出授權同步處理清單。

</dd> <dt>

*pcbSyncList* \[擴展\]
</dt> <dd>

授權同步清單的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDDRMSP .idl</dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMDevice 介面**](iwmdrmdevice.md)
</dt> </dl>

 

 





