---
title: 'Session 物件 (WSManDisp) '
description: 定義作業和會話設定。
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- 會話物件 Windows 遠端管理
- 會話物件 Windows 遠端管理，說明
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935128"
---
# <a name="session-object-wsmandisph"></a>Session 物件 (WSManDisp) 

定義作業和會話設定。 任何 Windows 遠端管理作業都需要建立連接至遠端電腦、[*基礎管理控制器*](windows-remote-management-glossary.md) (BMC) 或本機電腦的 **會話**。 WinRM 網路作業包括取得、寫入或列舉資料，或叫用方法。 **Session** 物件的方法會鏡像 WS-Management 通訊協定中定義的基本作業。

## <a name="members"></a>成員

**Session** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Session** 物件有這些方法。



| 方法                                 | 描述                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**創建**](session-create.md)       | 建立資源的新實例，並傳回新物件的 URI。<br/>                                      |
| [**刪除**](session-delete.md)       | 刪除資源 URI 中指定的資源。<br/>                                                              |
| [**列舉**](session-enumerate.md) | 列舉集合、資料表或訊息記錄資源。<br/>                                                         |
| [**Get**](session-get.md)             | 從服務抓取資源，並傳回目前資源實例的 XML 標記法。<br/> |
| [**識別**](session-identify.md)   | 查詢遠端電腦，以判斷它是否支援 WS-Management 的通訊協定<br/>                                 |
| [**調用**](session-invoke.md)       | 叫用方法，這個方法會傳回方法呼叫的結果。<br/>                                                    |
| [**把**](session-put.md)             | 更新資源。<br/>                                                                                              |



 

### <a name="properties"></a>屬性

**Session** 物件具有這些屬性。



| 屬性                                            | 存取類型           | Description                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchItems**](session-batchitems.md)<br/> | 讀取/寫入<br/> | 設定並取得每個列舉批次中的專案數。 列舉期間無法變更此值。 依預設，預設為不限數目的專案。 資源提供者可能會設定限制。<br/> |
| [**錯誤**](session-error.md)<br/>           | 唯讀<br/>  | 取得 XML 資料流程中的其他錯誤資訊。<br/>                                                                                                                                                              |
| [**超時**](session-timeout.md)<br/>       | 讀取/寫入<br/> | 設定並取得用戶端應用程式等候的最大時間量（以毫秒為單位） () 。<br/>                                                                                                                   |



 

## <a name="remarks"></a>備註

**會話** 物件會對應至 [**iwsmansession.invoke**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)介面。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例顯示如何建立 **會話** 物件。


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WinRM 腳本 API](winrm-scripting-api.md)
</dt> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)
</dt> <dt>

[從本機電腦取得資料](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[從遠端電腦取得資料](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





