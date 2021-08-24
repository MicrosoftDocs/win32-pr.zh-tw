---
description: 安裝程式物件的 OpenDatabase 方法會開啟現有的資料庫，或建立一個新的資料庫，並傳回資料庫物件。 如果無法成功建立和開啟資料庫物件，它就會產生錯誤。
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: OpenDatabase 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: aab1e66dd4208817f854db88c57db5b6269a7a0b912242da649dffcf24cabab3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821368"
---
# <a name="installeropendatabase-method"></a>OpenDatabase 方法

[**安裝程式**](installer-object.md)物件的 **OpenDatabase** 方法會開啟現有的資料庫，或建立一個新的資料庫，並傳回 [**資料庫**](database-object.md)物件。 如果無法成功建立和開啟 **資料庫** 物件，它就會產生錯誤。

## <a name="syntax"></a>語法


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*name* 
</dt> <dd>

必要的字串，其中包含資料庫的路徑名稱。 如果提供空字串，則會建立不會保存的暫存資料庫。

</dd> <dt>

*openMode* 
</dt> <dd>

下列清單中的參數，或字串，其中包含要在認可時寫入之新輸出資料庫檔案的路徑名稱。



| 參數                                                                                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt> </dl>                 | 開啟資料庫唯讀，無持續性變更。<br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt> </dl>                 | 在交易模式中開啟資料庫的讀取/寫入。<br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt> </dl>                         | 開啟無交易的資料庫直接讀取/寫入。<br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt> </dl>                         | 建立新的資料庫（交易模式讀取/寫入）。<br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt> </dl> | 建立新的資料庫，直接模式讀取/寫入。<br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt> </dl>         | 開啟資料庫以查看公告腳本檔，例如 [**CreateAdvertiseScript**](installer-createadvertisescript.md) 方法所產生的檔案。<br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt> </dl>            | 新增此旗標以表示修補檔案。<br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

代表已開啟之現有或新安裝程式資料庫的 [**資料庫**](database-object.md) 物件。

## <a name="remarks"></a>備註

當資料庫開啟為另一個資料庫的輸出時，輸出資料庫的摘要資訊資料流程實際上是原始資料庫的唯讀鏡像，因此無法變更。 此外，它也不會與資料庫一起保存。 若要建立或修改輸出資料庫的摘要資訊，必須將其關閉並重新開啟。

若要進行並儲存資料庫的變更，請先在交易 (msiOpenDatabaseModeTransact) 中開啟資料庫，並建立 (msiOpenDatabaseModeCreate 或 msiOpenDatabaseModeCreateDirect) ，或直接 (msiOpenDatabaseModeDirect) 模式。 進行變更之後，請一律在關閉資料庫控制碼之前呼叫 [**Commit**](database-commit.md) 方法。 **Commit** 方法會清空所有緩衝區。

請一律在關閉資料庫之前 (msiOpenDatabaseModeDirect 或 msiOpenDatabaseModeCreateDirect) 在直接模式中開啟的資料庫上，呼叫 [**Commit**](database-commit.md) 方法或。 若無法這樣做，可能會損毀資料庫。

由於 **OpenDatabase** 方法會起始資料庫存取，因此不能與執行中的安裝一起使用。

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




