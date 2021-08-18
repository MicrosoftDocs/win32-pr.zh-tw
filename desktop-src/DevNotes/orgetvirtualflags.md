---
description: 抓取離線登錄區中指定的開啟登錄機碼上的虛擬旗標。
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: 'ORGetVirtualFlags 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 8f0e44c388b576bb514ed86f2a537cefaf1a4f0984e3e5beb1b466e88c5b82c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076052"
---
# <a name="orgetvirtualflags-function"></a>ORGetVirtualFlags 函式

抓取離線登錄區中指定的開啟登錄機碼上的虛擬旗標。

## <a name="syntax"></a>語法


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> <dt>

*pdwFlags* \[擴展\]
</dt> <dd>

變數的指標，用來接收為機碼設定的虛擬旗標。 函數傳回之後，這個參數可以是下列其中一個或多個值。



| 值                                                                                                                                                                                                                                                    | 意義                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**REG \_機碼不是 \_ \_ 無訊息 \_ 失敗**</dt> <dt>4</dt> </dl> | 如果設定此旗標，且已啟用虛擬化的金鑰上的開啟作業失敗，則登錄不會嘗試重新開啟金鑰。 如果清除此旗標，登錄會嘗試以允許的最大存取權重新開啟金鑰 \_ 。<br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**REG \_機碼不會 \_ \_ 虛擬化**</dt> <dt>2</dt> </dl>     | 如果設定此旗標，且建立索引鍵作業失敗，因為呼叫端沒有父索引鍵的 KEY \_ Create \_ SUB \_ key，則登錄會使建立作業失敗。 如果清除此旗標，登錄會嘗試在虛擬存放區中建立金鑰。 呼叫 \_ 端必須在父機碼上具有讀取權限。<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**REG \_按鍵 \_ 遞迴 \_ 旗**</dt>標 <dt>8</dt> </dl>              | 如果設定此旗標，則會從父機碼傳播登錄虛擬旗標。 如果清除此旗標，則不會傳播登錄虛擬旗標。<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

## <a name="remarks"></a>備註

登錄虛擬化是一項過渡的應用程式相容性技術，可讓具有全域影響的登錄寫入作業重新導向至每個使用者的位置。 對於讀取或寫入登錄的應用程式而言，此重新導向是透明的。

從 Windows Vista 開始支援登錄虛擬化。 不過，Microsoft 打算將它從未來的 Windows 作業系統版本中移除，因為更多應用程式都與 Windows Vista 相容。 因此，應用程式不應該依賴系統中的登錄虛擬化行為。

登錄虛擬化只會針對下列各項啟用：

-   32位互動式進程
-   **HKEY \_ 本機 \_ 電腦 \\ 軟體** 中的金鑰
-   系統管理員可寫入的金鑰

如需詳細資訊，請參閱登錄 [虛擬化](../sysinfo/registry-virtualization.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows離線登錄庫1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORSetVirtualFlags**](orsetvirtualflags.md)
</dt> <dt>

[登錄虛擬化](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
