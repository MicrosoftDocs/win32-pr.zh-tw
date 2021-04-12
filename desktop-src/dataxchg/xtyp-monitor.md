---
title: 'XTYP_MONITOR 交易 (Ddeml .h) '
description: 當系統中發生 DDE 事件時，動態資料交換 (DDE) 偵錯工具的 DDE 回呼函式 DdeCallback 接收 XTYP \_ 監視器交易。
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- XTYP_MONITOR 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384434"
---
# <a name="xtyp_monitor-transaction"></a>XTYP \_ 監視交易

當系統中發生 DDE 事件時，動態資料交換 (DDE) 偵錯工具的 DDE 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)接收 **XTYP \_ 監視器** 交易。 若要接收此交易，應用程式必須在呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式時指定 **APPCLASS \_ 監視器** 值。


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>參數

<dl> <dt>

*uType* 
</dt> <dd>

交易類型。

</dd> <dt>

*uFmt* 
</dt> <dd>

未使用。

</dd> <dt>

*hconv* 
</dt> <dd>

未使用。

</dd> <dt>

*hsz1* 
</dt> <dd>

未使用。

</dd> <dt>

*hsz2* 
</dt> <dd>

未使用。

</dd> <dt>

*hdata* 
</dt> <dd>

DDE 物件的控制碼，其中包含有關 DDE 事件的資訊。 應用程式應該使用 [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) 函式來取得物件的指標。

</dd> <dt>

*dwData1* 
</dt> <dd>

未使用。

</dd> <dt>

*dwData2* 
</dt> <dd>

DDE 事件。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                      | 意義                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <dt>**MF \_回呼**</dt> <dt>0x08000000</dt> </dl> | 系統會將交易傳送至 DDE 回呼函數。 DDE 物件包含 [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) 結構，可提供交易的相關資訊。<br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <dt>**MF \_約定**</dt> <dt>0x40000000</dt> </dl>                | 已建立或終止 DDE 交談。 DDE 物件包含提供交談相關資訊的 [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) 結構。<br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <dt>**MF \_錯誤**</dt> <dt>0x10000000</dt> </dl>          | 發生 DDE 錯誤。 DDE 物件包含 [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) 結構，提供錯誤的相關資訊。<br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <dt>**MF \_HSZ \_ INFO**</dt> <dt>0x01000000</dt> </dl>   | DDE 應用程式建立、釋放或遞增字串控制碼的使用計數，或字串控制碼因為呼叫 [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) 函式而釋出。 DDE 物件包含 [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) 結構，提供字串控制碼的相關資訊。<br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <dt>**MF \_連結**</dt> <dt>0x20000000</dt> </dl>             | DDE 應用程式已啟動或停止「建議」迴圈。 DDE 物件包含 [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) 結構，提供建議迴圈的相關資訊。<br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <dt>**MF \_POSTMSGS**</dt> <dt>0x04000000</dt> </dl>    | 已張貼 DDE 訊息的系統或應用程式。 DDE 物件包含提供訊息相關資訊的 [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) 結構。<br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <dt>**MF \_SENDMSGS**</dt> <dt>0x02000000</dt> </dl>    | 系統或應用程式傳送了 DDE 訊息。 DDE 物件包含提供訊息相關資訊的 [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) 結構。<br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果回呼函式處理此交易，它應該會傳回0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Ddeml (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

