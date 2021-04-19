---
title: ITSRemoteProgram RemoteProgramMode 屬性
description: Windows Server 2008 R2 RemoteApp 模式。
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- RemoteProgramMode 屬性遠端桌面服務
- RemoteProgramMode 屬性遠端桌面服務，ITSRemoteProgram 介面
- ITSRemoteProgram 介面遠端桌面服務，RemoteProgramMode 屬性
- RemoteProgramMode 屬性遠端桌面服務，ITSRemoteProgram2 介面
- ITSRemoteProgram2 介面遠端桌面服務，RemoteProgramMode 屬性
- RemoteProgramMode 屬性遠端桌面服務，ITSRemoteProgram3 介面
- ITSRemoteProgram3 介面遠端桌面服務，RemoteProgramMode 屬性
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983314"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>ITSRemoteProgram：： RemoteProgramMode 屬性

Windows Server 2008 R2 RemoteApp 模式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a>屬性值

RemoteApp 模式。 如果設定為 **VARIANT \_ TRUE**，則會啟用 remoteapp 模式，而遠端會話將會裝載 remoteapp 程式。 如果設定為 **VARIANT \_ FALSE** (預設) ，則不會啟用 RemoteApp 模式。 遠端會話將裝載遠端桌面。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram 定義為 FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





