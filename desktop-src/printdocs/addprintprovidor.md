---
description: AddPrintProvidor 函式會安裝本機列印提供者，並連結設定、資料和提供者檔案。
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: 'AddPrintProvidor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ca968397441765455e74059201c128be53f50916e5e28212c700078f52124fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868733"
---
# <a name="addprintprovidor-function"></a>AddPrintProvidor 函式

**AddPrintProvidor** 函式會安裝本機列印提供者，並連結設定、資料和提供者檔案。

## <a name="syntax"></a>語法


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定應該安裝提供者之伺服器的名稱。 針對僅支援提供者本機安裝的系統，此參數應為 **Null**。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PProviderInfo* 所指向之結構的層級。 它可以是下列其中一項。



| 值                                                                                                | 意義                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 函數會使用 [**PROVIDOR \_ INFO \_ 1**](providor-info-1.md) 結構。<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 函數會使用 [**PROVIDOR \_ INFO \_ 2**](providor-info-2.md) 結構。<br/> |



 

</dd> <dt>

*pProviderInfo* \[在\]
</dt> <dd>

列印提供者結構的指標，由 *層級* 表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

在應用程式呼叫 **AddPrintProvidor** 函式之前，提供者所需的所有檔案都必須複製到 SYSTEM32 目錄。

藉由呼叫 [**DeletePrintProvidor**](deleteprintprovidor.md)，可移除 **AddPrintProvidor** 所新增的提供者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **AddPrintProvidorW** (Unicode) 和 **AddPrintProvidorA** (ANSI) <br/>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrintProvidor**](deleteprintprovidor.md)
</dt> <dt>

[**PROVIDOR \_ 資訊 \_ 1**](providor-info-1.md)
</dt> <dt>

[**PROVIDOR \_ 資訊 \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




