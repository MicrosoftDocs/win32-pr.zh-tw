---
description: 安裝程式物件的 EnableLog 方法，可針對目前進程空間中的所有後續安裝會話，記錄所選取的訊息類型。
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: EnableLog 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975747"
---
# <a name="installerenablelog-method"></a>EnableLog 方法

[**安裝程式**](installer-object.md)物件的 **EnableLog** 方法，可針對目前進程空間中的所有後續安裝會話，記錄所選取的訊息類型。

## <a name="syntax"></a>語法


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*logMode* 
</dt> <dd>

必要的字串，其中包含代表要記錄之訊息類型的字母。 字串可以是下列值的組合。



| 值 | 描述                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | 僅限資訊的訊息。                                                                             |
| w     | 非嚴重警告訊息。                                                                            |
| e     | 可能是嚴重錯誤的錯誤訊息。                                                               |
| f     | 使用中需要取代的檔案清單。                                                         |
| a     | 開始動作通知。                                                                          |
| r     | 動作資料記錄，其中包含動作特定的內容。                                              |
| u     | 使用者要求訊息。                                                                                 |
| c     | UI 初始化參數。                                                                          |
| m     | 記憶體不足的訊息。                                                                                 |
| v     | 將大量資訊傳送至記錄檔，對使用者而言通常不實用。 可以用來提供支援。 |
| p     | 傾印屬性工作表;引擎終止時的 "property = value"                                          |
| \+    | 附加至現有的記錄檔。                                                                           |
| !     | 將每一行排清到記錄檔。                                                                       |
| x     | 額外的調試資訊。 此選項僅適用于 Windows Server 2003。                      |
| o     | 磁碟空間不足的訊息。                                                                            |



 

</dd> <dt>

*記錄檔* 
</dt> <dd>

必要的字串，其中包含要建立之記錄檔的路徑。 使用空字串 ( "" ) 來關閉記錄。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

使用這個方法時，記錄檔位置的路徑必須已經存在。 安裝程式不會建立記錄檔的目錄結構。

使用 **EnableLog** 所設定的記錄選項會覆寫任何現有的 Windows Installer 記錄原則設定。

記錄預設會覆寫現有的記錄檔。 您必須在記錄模式中使用 ' + ' 字母，以附加至現有的記錄檔。

不建議使用 '！ ' 選項，因為它可能會大幅降低安裝速度。 在對安裝進行偵錯工具時，此選項可能很有用。

下列範例腳本會開啟安裝的詳細資訊記錄。 在安裝結束時，產生的記錄檔將會是 c： \\ temp \\ install .log。


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows Installer 記錄](windows-installer-logging.md)
</dt> </dl>

 

 




