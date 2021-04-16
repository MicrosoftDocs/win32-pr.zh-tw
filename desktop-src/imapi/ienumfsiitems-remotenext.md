---
title: IEnumFsiItems RemoteNext 方法
description: 支援遠端用戶端，該用戶端想要取得列舉順序中指定的專案數。 |IEnumFsiItems RemoteNext 方法
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- RemoteNext 方法 IMAPI.EXE
- RemoteNext 方法 IMAPI.EXE、IEnumFsiItems 介面
- IEnumFsiItems 介面 IMAPI.EXE，RemoteNext 方法
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514468"
---
# <a name="ienumfsiitemsremotenext-method"></a>IEnumFsiItems：： RemoteNext 方法

支援遠端用戶端，該用戶端想要取得列舉順序中指定的專案數。

## <a name="syntax"></a>語法


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*celt* \[在\]
</dt> <dd>

要取出的專案數目。

</dd> <dt>

*rgelt* \[擴展\]
</dt> <dd>

[**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem)介面的陣列。 完成時，您必須在 rgelt 中釋放每個介面。

</dd> <dt>

*pceltFetched* \[擴展\]
</dt> <dd>

在 rgelt 中傳回的元素數目。 如果 *celt* 是一個，您可以將 *PceltFetched* 設定為 **Null** 。 否則，在呼叫這個方法之前，請先將 *pceltFetched* 的值初始化為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_當 (*celt*) 的要求元素數目成功傳回，或 (*pceltFetched*) 的傳回專案數目小於要求的元素數目時，就會傳回 S OK。

可能會因為執行結果而傳回其他成功碼。 下列錯誤碼通常會在作業失敗時傳回，但不代表唯一可能的錯誤值：



| 傳回碼                                                                                   | Description                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 指標無效。<br/> 值：且顯示0x80004003<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 無法配置所需的記憶體。<br/> 值：0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 一或多個引數無效。<br/> 值：0x80070057<br/>    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| Idl<br/>                      | <dl> <dt>Imapi2fs .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumFsiItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[IEnumFsiItems：： Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





