---
title: 使用宏進行錯誤處理
description: COM 會定義許多宏，讓您更輕鬆地使用 HRESULT 值。
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f31280ec2076f8ece1fcf15dd6e27629a3016e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480534"
---
# <a name="using-macros-for-error-handling"></a>使用宏進行錯誤處理

COM 會定義許多宏，讓您更輕鬆地使用 **HRESULT** 值。

下表將說明錯誤處理宏。




| 巨集 | Description | 
|-------|-------------|
| <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br /> | 傳回包含<strong>hresult</strong>的嚴重性位、設備碼和錯誤碼的<strong>HRESULT</strong> 。<br /><blockquote>[!Note]<br />針對 S_OK 驗證呼叫 <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> 會帶來效能上的負面影響。 您不應該定期使用 <strong>MAKE_HRESULT</strong> 來取得成功的結果。</blockquote><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br /> | 傳回 <strong>SCODE</strong> ，指定包含 <strong>SCODE</strong>的嚴重性位、設施碼和錯誤碼。<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br /> | 解壓縮 <strong>HRESULT</strong>的錯誤碼部分。<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br /> | 解壓縮 <strong>HRESULT</strong>的設備程式碼。<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br /> | 解壓縮 <strong>HRESULT</strong>的嚴重性位。<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br /> | 解壓縮 <strong>SCODE</strong>的錯誤碼部分。<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br /> | 將 <strong>SCODE</strong>的設備碼解壓縮。<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br /> | 將 <strong>SCODE</strong>的嚴重性欄位解壓縮。<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>成功</strong></a><br /> | 測試 <strong>SCODE</strong> 或 <strong>HRESULT</strong>的嚴重性位;如果嚴重性為零，則傳回 <strong>TRUE</strong> ，如果是，則傳回 <strong>FALSE</strong> 。<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>失敗</strong></a><br /> | 測試 <strong>SCODE</strong> 或 <strong>HRESULT</strong>的嚴重性位;如果嚴重性是1，則傳回 <strong>TRUE</strong> ，如果是零，則傳回 <strong>FALSE</strong> 。<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br /> | 提供任何狀態值的一般測試錯誤。 <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br /> | 地圖<a href="/windows/desktop/Debug/system-error-codes">系統錯誤碼</a>至<strong>HRESULT</strong>值。 <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br /> | 地圖 NT 狀態值設為<strong>HRESULT</strong>值。<br /> | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的錯誤處理](error-handling-in-com.md)
</dt> </dl>

 

