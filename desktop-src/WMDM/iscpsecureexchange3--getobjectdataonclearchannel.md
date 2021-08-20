---
title: GetObjectDataOnClearChannel 方法
description: GetObjectDataOnClearChannel 方法會將清除通道上的物件資料區區塊轉送回 Windows 媒體裝置管理員。
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- GetObjectDataOnClearChannel 方法 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10e09697653c2ef1235ae9a3ea3a93a45437d1cf45a1f4de72ec99b0812b9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619868"
---
# <a name="getobjectdataonclearchannel-method"></a>GetObjectDataOnClearChannel 方法

**GetObjectDataOnClearChannel** 方法會將清除通道上的物件資料區區塊轉送回 Windows 媒體裝置管理員。

此方法與 [**ISCPSecureExchange：： ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) 相同，不同之處在于這個方法所傳回的資料並未加密。 因此，這個方法更有效率。

## <a name="syntax"></a>語法


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* 
</dt> <dd>

裝置物件的指標。

</dd> <dt>

*.Pdata* 
</dt> <dd>

用來接收資料的緩衝區指標。

</dd> <dt>

*pdwSize* 
</dt> <dd>

包含傳輸大小的 **DWORD** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果方法失敗，則會傳回 **HRESULT** 錯誤碼。



| 傳回碼                                                                                                | 描述                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**WMDM \_ E \_ MAC \_ 檢查 \_ 失敗**</dt> </dl> | 訊息驗證碼無效。<br/>                                    |
| <dl> <dt>**WMDM \_ E \_ NORIGHTS**</dt> </dl>           | 呼叫端沒有執行要求的作業所需的許可權。<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | 方法失敗。 終止與內容提供者的互動。<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | 參數是無效或 **Null** 指標。<br/>                                   |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                     | 發生未指定的錯誤。<br/>                                                   |



 

## <a name="remarks"></a>備註

若要傳送資料，Windows Media 裝置管理員呼叫[TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel)方法來取得容器資料。 接著會呼叫 **GetObjectDataOnClearChannel** ，將物件資料的區塊從內容提供者傳送至 Windows 媒體裝置管理員。 如果將 \_ *pdwSize* 設為零，傳回 S OK，Windows Media 裝置管理員將不會要求進一步的資料。

此方法與 [**ISCPSecureExchange：： ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) 相同，不同之處在于這個方法所傳回的資料並未加密。 因此，這個方法更有效率。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>WMSCP .idl</dt> </dl>    |
| 程式庫<br/> | <dl> <dt>Mssachlp .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCPSecureExchange：： ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**ISCPSecureExchange3 介面**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





