---
title: IMsRdpClientShell 啟動方法
description: 從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動遠端檔案內容。
ms.assetid: a0aa12e4-8b6f-4a3a-a6b8-f5def0b8bd90
ms.tgt_platform: multiple
keywords:
- 啟動方法遠端桌面服務
- 啟動方法遠端桌面服務，IMsRdpClientShell 介面
- IMsRdpClientShell 介面遠端桌面服務，啟動方法
topic_type:
- apiref
api_name:
- IMsRdpClientShell.Launch
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae895d8a12824c6aca1dcbd69c5055b3ca6f3e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384177"
---
# <a name="imsrdpclientshelllaunch-method"></a>IMsRdpClientShell：：啟動方法

從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動遠端檔案內容。

## <a name="syntax"></a>語法


```C++
HRESULT Launch();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell 定義為 d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





