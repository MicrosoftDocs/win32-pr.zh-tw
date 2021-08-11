---
title: 'MpFreeMemory 函式 (MpClient) '
description: 釋出 malware protection manager 的記憶體。
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- MpFreeMemory 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 806795cee45fcfe95473c0961106da074c1157b65ac5c19f5d4813c84865616a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247423"
---
# <a name="mpfreememory-function"></a>MpFreeMemory 函式

釋出 malware protection manager 的記憶體。 惡意程式碼防護函式所配置和傳回的所有緩衝區都必須由呼叫者使用此函式釋放。

## <a name="syntax"></a>語法


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMemory* \[在\]
</dt> <dd>

類型： **PVOID**

惡意程式碼防護功能所配置之記憶體的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

為了加速用戶端的記憶體管理，malware protection manager 也會定義宏來釋出與惡意程式碼防護功能所傳回之各種結構相關聯的記憶體。 下列巨集定義在標頭檔 mpmemfree 中：



| 名稱                            | 描述                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| \_免費 MPRESOURCE 資訊 \_          | 釋出已配置的 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。                  |
| \_免費 MPTHREAT 資訊 \_            | 釋出已配置的 [**MPTHREAT \_ 資訊**](mpthreat-info.md)。                      |
| \_免費 MPTHREAT 當地語系化 \_ 資訊 \_ | 釋出已配置的 [**MPTHREAT \_ 當地語系化 \_ 資訊**](mpthreat-localized-info.md)。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MPRESOURCE \_ 資訊**](mpresource-info.md)
</dt> <dt>

[**MPTHREAT \_ 資訊**](mpthreat-info.md)
</dt> <dt>

[**MPTHREAT \_ 當地語系化的 \_ 資訊**](mpthreat-localized-info.md)
</dt> </dl>

 

 





