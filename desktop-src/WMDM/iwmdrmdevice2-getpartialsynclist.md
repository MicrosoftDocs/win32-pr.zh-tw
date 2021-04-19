---
title: IWMDRMDevice2 GetPartialSyncList 方法
description: GetPartialSyncList 方法會取得部分同步處理清單。
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- GetPartialSyncList 方法 windows Media 裝置管理員
- GetPartialSyncList 方法 windows Media 裝置管理員，IWMDRMDevice2 介面
- IWMDRMDevice2 interface windows Media 裝置管理員，GetPartialSyncList 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996040"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>IWMDRMDevice2：： GetPartialSyncList 方法

**GetPartialSyncList** 方法會取得部分同步處理清單。

## <a name="syntax"></a>語法


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
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

*dwStartingIndex* \[在\]
</dt> <dd>

索引的開始位置。

</dd> <dt>

*cItems* \[在\]
</dt> <dd>

要編制索引的專案計數。

</dd> <dt>

*ppbSyncList* \[擴展\]
</dt> <dd>

已取出授權同步處理清單。

</dd> <dt>

*pcbSyncList* \[擴展\]
</dt> <dd>

授權同步清單的大小（以位元組為單位）。

</dd> <dt>

*pdwNextStartingIndex* \[擴展\]
</dt> <dd>

索引的下一個開始位置。

</dd> <dt>

*pcItemsProcessed* \[擴展\]
</dt> <dd>

正在處理的專案計數。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 Windows Media 裝置管理員中的所有介面方法都可以傳回下列任何錯誤碼類別：

-   標準 COM 錯誤碼
-   轉換成 HRESULT 值的 Windows 錯誤碼
-   Windows Media 裝置管理員錯誤碼

如需可能錯誤碼的詳細清單，請參閱 [錯誤碼](error-codes.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMDDRMSP .idl</dt> </dl> |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMDevice::GetSyncList**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**IWMDRMDevice2 介面**](iwmdrmdevice2.md)
</dt> </dl>

 

 





