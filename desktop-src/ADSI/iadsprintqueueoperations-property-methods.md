---
title: 'IADsPrintQueueOperations 屬性方法 (Iads .h) '
description: IADsPrintQueueOperations 介面的屬性方法會讀取並寫入下列清單中列出的屬性。 如需屬性方法的詳細資訊，請參閱介面屬性方法。
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- IADsPrintQueueOperations 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c0438491cb62d56584106d78f7639439d93d105fb635eeba0271759247f595
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839758"
---
# <a name="iadsprintqueueoperations-property-methods"></a>IADsPrintQueueOperations 屬性方法

[**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)介面的屬性方法會讀取並寫入下列清單中列出的屬性。 如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**狀態**
</dt> <dd> <dl>

列印佇列作業的目前狀態。 有效的狀態碼值會列在下列清單中。

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

**廣告 \_已 \_ 暫停印表機** (0x00000001) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

**廣告 \_印表機 \_ 暫止 \_ 刪除** (0x00000002) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

**廣告 \_印表機 \_ 錯誤** (0x00000003) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

**廣告 \_印表機 \_ 紙 \_ 卡** (0x00000004) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

**廣告 \_印表機 \_ 紙 \_** (0x00000005) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

**廣告 \_印表機 \_ 手動 \_ 饋送** (0x00000006) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

**廣告 \_印表機 \_ 紙張 \_ 問題** (0x00000007) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

**廣告 \_印表機 \_ 離線** (0x00000008) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

**廣告 \_印表機 \_ IO \_ 主動** (0x00000100) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

**廣告 \_印表機 \_ 忙碌** (0x00000200) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

**廣告 \_印表機 \_ 列印** (0x00000400) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

**廣告 \_印表機 \_ 輸出 \_ BIN \_ FULL** (0x00000800) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

**廣告 \_印表機 \_ 無法 \_ 使用** (0x00001000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

**廣告 \_印表機 \_ 正在等候** (0x00002000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

**廣告 \_印表機 \_ 處理** (0x00004000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

**廣告 \_ (\_** 0x00008000) 的印表機初始化


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

**廣告 \_印表機 \_ 預熱 \_** (0x00010000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

**廣告 \_印表機 \_ 墨粉 \_ 低** (0x00020000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

**廣告 \_印表機 \_ 沒有 \_ 碳粉** (0x00040000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

**廣告 \_印表機 \_ 頁面 \_** (0x00080000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

**廣告 \_ (0x00100000) 的印表機 \_ 使用者 \_ 介入**


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

**廣告 \_印表機 \_ \_ \_ 記憶體** (0x00200000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

**廣告 \_印表機 \_ 門 \_ 開啟** (0x00400000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

**廣告 \_印表機 \_ 伺服器 \_ 不明** (0x00800000) 


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

**廣告 \_印表機 \_ 電源 \_ 節省** (0x01000000) 


</dt> <dd></dd> </dl> <dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>範例

下列 Visual Basic 程式碼範例會驗證印表機是否已卡住。


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



下列 c + + 程式碼範例會驗證印表機是否已卡住。


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IADsPrintQueueOperations 定義為124BE5C0-156E-11CF-A986-00AA006BC149<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





