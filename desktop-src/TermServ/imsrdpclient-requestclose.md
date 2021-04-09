---
title: IMsRdpClient RequestClose 方法
description: 要求遠端桌面 ActiveX 控制項正常關機。
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- RequestClose 方法遠端桌面服務
- RequestClose 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，RequestClose 方法
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685676"
---
# <a name="imsrdpclientrequestclose-method"></a>IMsRdpClient：： RequestClose 方法

要求遠端桌面 ActiveX 控制項正常關機。 正常關機可以包括結束使用者的遠端桌面服務會話，但不會將遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。

## <a name="syntax"></a>語法


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCloseStatus* \[擴展\]
</dt> <dd>

[**ControlCloseStatus**](controlclosestatus.md)列舉中的值，指出應用程式是否可以立即關閉控制項。 以下是可能值的清單。

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000) 


</dt> <dd>

容器應用程式可以繼續立即關閉控制項。 這個值也可以表示連接已經結束。

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001) 


</dt> <dd>

容器應用程式不應立即關閉控制項;應用程式應該等候下列備註區段中所述的其中一個事件在關閉之前發生。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

如果 *pCloseStatus* 參數等於 **controlCloseWaitForEvents**，應用程式應該在應用程式關閉控制項之前，等候下列其中一個事件發生：

-   [**IMsTscAxEvents：： OnDisconnected**](imstscaxevents-ondisconnected.md)。 如果使用者未登入遠端桌面服務的會話，則應用程式可以呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 函式來摧毀所有視窗，然後關閉控制項。
-   [**IMsTscAxEvents：： OnConfirmClose**](imstscaxevents-onconfirmclose.md)。 如果使用者登入遠端桌面服務會話，控制項就會引發 **OnConfirmClose** 事件。 此事件可讓應用程式提示使用者是否要關閉連接。 如果使用者對提示回復 [是]，容器應用程式可以呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 來終結所有視窗，然後關閉控制項。

**RequestClose** 可讓容器應用程式提示使用者是否要關閉連接。 如需詳細資訊，請參閱 [**IMsTscAxEvents：： OnConfirmClose**](imstscaxevents-onconfirmclose.md)。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

