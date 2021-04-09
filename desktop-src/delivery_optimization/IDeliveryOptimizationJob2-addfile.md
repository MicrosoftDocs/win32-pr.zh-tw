---
title: IDeliveryOptimizationJob2 AddFile 方法
description: AddFile 方法會將單一檔案新增至現有的作業。
keywords:
- AddFile 方法
- AddFile 方法，IDeliveryOptimizationJob2 介面
- IDeliveryOptimizationJob2 介面，AddFile 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094195"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>IDeliveryOptimizationJob2：： AddFileWithRanges 方法

AddFile 方法會將單一檔案新增至現有的作業。

## <a name="syntax"></a>語法

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*fileId* \[在\]
</dt> <dd>

檔案識別碼字串，可唯一識別要下載的檔案。

</dd> <dt>

*remoteUrl* \[在\]
</dt> <dd>

將嘗試連接以下載檔案的檔案 URL。

</dd> <dt>

*rangeCount* \[在\]
</dt> <dd>

*範圍* 中包含的專案數目。 零值表示沒有任何範圍用於檔案。

</dd> <dt>

*範圍* \[在\]
</dt> <dd>

選用的範圍清單。 清單中的每個範圍都是 [**BG_FILE_RANGE**](bg-file-range.md) 結構。

</dd> <dt>

*riid* \[在\]
</dt> <dd>

物件中包含的物件類型。 這必須由類型 IID_IDeliveryOptimizationFile。

</dd> <dt>

*物件* \[擴展\]
</dt> <dd>

IDeliveryOptimizationFile 物件，代表下載檔案。 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會在成功時傳回 S_OK，或在發生錯誤時傳回其中一個標準 HRESULT 值。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|---------------------------|---------------------------------------------------------------------------------|
| 最低支援的用戶端  | Windows 10， \[ 僅限1803版桌面應用程式\]                                  |
| 最低支援的伺服器  | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]                              |
| 標頭                    | >deliveryoptimization。h                                                          |
| Idl                       | >deliveryoptimization .idl                                                        |
| 程式庫                   | Dosvc .lib                                                                       |
| DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob 定義為 EE2584CF-A69C-4848-B633-2649962B3EF7 |

## <a name="see-also"></a>另請參閱

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
