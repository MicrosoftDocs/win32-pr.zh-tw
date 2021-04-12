---
title: ITSRemoteProgram 介面
description: 包含用來設定和取出 remoteapp 模式的方法，以及 RemoteApp 程式的啟動參數，例如可執行檔和工作目錄的路徑。
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- ITSRemoteProgram 介面遠端桌面服務
- ITSRemoteProgram 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025237"
---
# <a name="itsremoteprogram-interface"></a>ITSRemoteProgram 介面

包含用來設定和取出 remoteapp 模式的方法，以及 RemoteApp 程式的啟動參數，例如可執行檔和工作目錄的路徑。

## <a name="members"></a>成員

**ITSRemoteProgram** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITSRemoteProgram** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ITSRemoteProgram** 介面具有這些方法。



| 方法                                                            | 描述                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**ServerStartProgram**](itsremoteprogram-serverstartprogram.md) | 指定要在遠端會話中啟動的 RemoteApp 程式。<br/> |



 

### <a name="properties"></a>屬性

**ITSRemoteProgram** 介面具有這些屬性。



| 屬性                                                                   | 存取類型           | Description                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [**RemoteProgramMode**](itsremoteprogram-remoteprogrammode.md)<br/> | 讀取/寫入<br/> | RemoteApp 模式。<br/> |



 

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

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

