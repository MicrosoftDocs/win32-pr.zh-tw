---
title: ITSRemoteProgram ServerStartProgram 方法
description: 指定要在遠端會話中啟動的 RemoteApp 程式。
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- ServerStartProgram 方法遠端桌面服務
- ServerStartProgram 方法遠端桌面服務，ITSRemoteProgram 介面
- ITSRemoteProgram 介面遠端桌面服務，ServerStartProgram 方法
- ServerStartProgram 方法遠端桌面服務，ITSRemoteProgram2 介面
- ITSRemoteProgram2 介面遠端桌面服務，ServerStartProgram 方法
- ServerStartProgram 方法遠端桌面服務，ITSRemoteProgram3 介面
- ITSRemoteProgram3 介面遠端桌面服務，ServerStartProgram 方法
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c789a9963086128e93546415247cfb3db69afe59c67a445b851ee5cf3687d16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756854"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>ITSRemoteProgram：： ServerStartProgram 方法

指定要在遠端會話中啟動的 RemoteApp 程式。 當用戶端) 收到會話連線通知之後，就必須在連線的會話上叫用此函數 (。 任何數目的 RemoteApp 程式都可以在會話中啟動。 如果會話中沒有任何 remoteapp 程式在超時時間限制內啟動（這是 Windows Server 2008 的兩分鐘）時，remoteapp 會話將會過期。

## <a name="syntax"></a>語法


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrExecutablePath* \[在\]
</dt> <dd>

伺服器上 RemoteApp 程式可執行檔的路徑。

</dd> <dt>

*bstrFilePath* \[在\]
</dt> <dd>

要在伺服器上透過檔案關聯開啟的檔案路徑，例如 "C： \\ \\ Documents \\ \\MyReport.docx"。 如果您指定 *bstrFilePath*，則不應指定 *bstrExecutablePath* 參數，反之亦然。 您應該只指定其中一個參數。

</dd> <dt>

*bstrWorkingDirectory* \[在\]
</dt> <dd>

適用于 RemoteApp 程式之伺服器上的工作目錄。

</dd> <dt>

*vbExpandEnvVarInWorkingDirectoryOnServer* \[在\]
</dt> <dd>

指出伺服器是否應在工作目錄路徑中展開環境變數。 如果工作目錄路徑包含環境變數，則將此參數設定為 **variant \_ TRUE** ，如果工作目錄路徑不包含環境變數，則為 **variant \_ FALSE** 。

</dd> <dt>

*bstrArguments* \[在\]
</dt> <dd>

在 *bstrExecutablePath* 中指定之 RemoteApp 程式的命令列引數。 如果未指定 *bstrExecutablePath* ，請將此值設定為 **Null** 。

</dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[在\]
</dt> <dd>

指出伺服器是否應展開命令列引數中的環境變數。 如果引數包含環境變數，則將此參數設定為 **variant \_ TRUE** ，如果引數不包含環境變數，則為 **variant \_ FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

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

 

 





