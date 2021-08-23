---
title: IMsTscAxEvents OnConfirmClose 方法
description: 當用戶端呼叫 IMsRdpClient RequestClose 方法時呼叫。
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- OnConfirmClose 方法遠端桌面服務
- OnConfirmClose 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnConfirmClose 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2effd50552ab227e8e065844b8b19da0e022f6b8e36d1d86701ad0614b821126
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512468"
---
# <a name="imstscaxeventsonconfirmclose-method"></a>IMsTscAxEvents：： OnConfirmClose 方法

當用戶端呼叫 [**IMsRdpClient：： RequestClose**](imsrdpclient-requestclose.md) 方法時呼叫。 為了回應此事件，系統應該會提示使用者確認關閉連接。 如需詳細資訊，請參閱接下來的＜備註＞一節。

## <a name="syntax"></a>語法


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pfAllowClose* \[擴展\]
</dt> <dd>

如果 **VARIANT \_ TRUE**（預設值）表示使用者想要關閉連接。 如果 **VARIANT \_ FALSE**，表示使用者不想關閉連接。 如需詳細資訊，請參閱接下來的＜備註＞一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當容器應用程式呼叫 [**IMsRdpClient：： RequestClose**](imsrdpclient-requestclose.md) 方法時，該方法會傳回一個值，指出容器是否應該在關閉控制項連接之前等候 **OnConfirmClose** 事件。 如果 **RequestClose** 傳回 **controlCloseWaitForEvents**，而且使用者已連接並登入遠端桌面服務會話，則會引發 **OnConfirmClose** 事件。 屆時，容器應用程式可以提示使用者，詢問使用者是否想要關閉連接。 如果使用者想要關閉連接，應用程式應該將 *pfAllowClose* 參數設定為 **VARIANT \_ TRUE** ，然後繼續關閉連接。 如果使用者不想要關閉，應用程式應該將 *pfAllowClose* 設定為 **VARIANT \_ FALSE** ，並讓連接保持開啟。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





