---
title: 'IMsRdpClient7 GetStatusText 方法 (Openservice .h) '
description: 抓取指定狀態碼的狀態文字。
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- GetStatusText 方法遠端桌面服務
- GetStatusText 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，GetStatusText 方法
- GetStatusText 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，GetStatusText 方法
- GetStatusText 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，GetStatusText 方法
- GetStatusText 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，GetStatusText 方法
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686068"
---
# <a name="imsrdpclient7getstatustext-method"></a>IMsRdpClient7：： GetStatusText 方法

抓取指定狀態碼的狀態文字。

## <a name="syntax"></a>語法


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*statusCode* \[在\]
</dt> <dd>

指定要取得其文字之狀態碼的 **UINT** 。

</dd> <dt>

*pBstrStatusText* \[退出，retval\]
</dt> <dd>

接收狀態文字之 **BSTR** 的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                     |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Openservice。h</dt> </dl> |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpClient7 定義為 b2a5b5ce-3461-444a-91d4-add26d070638<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





