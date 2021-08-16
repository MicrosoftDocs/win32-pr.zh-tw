---
Description: 記憶體保護選項如下：在記憶體中配置或保護頁面時，您必須指定下列其中一個值。 無法將保護屬性指派給頁面的一部分;只能指派給整個頁面。
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: " (WinNT. h) 的記憶體保護常數"
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 187e8e1f4e137823451771309c9cce19db2e7fbd9c5b57597b51cfc58ca61297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067688"
---
# <a name="memory-protection-constants"></a>記憶體保護常數

記憶體保護選項如下：在記憶體中配置或保護頁面時，您必須指定下列其中一個值。 無法將保護屬性指派給頁面的一部分;只能指派給整個頁面。

## <a name="example"></a>範例

```cpp
STDMETHODIMP CExtBuffer::FInit
    (
    ULONG cItemMax,     //@parm IN | Maximum number of items ever
    ULONG cbItem,       //@parm IN | Size of each item, in bytes
    ULONG cbPage        //@parm IN | Size of system page size (from SysInfo)
    )
{
    BYTE  *pb;

    m_cbReserved = ((cbItem *cItemMax) / cbPage + 1) *cbPage;
    m_rgItem = (BYTE *) VirtualAlloc( NULL, m_cbReserved, MEM_RESERVE, PAGE_READWRITE );

    if (m_rgItem == NULL)
        return ResultFromScode( E_OUTOFMEMORY );

    m_cbItem  = cbItem;
    m_dbAlloc = (cbItem / cbPage + 1) *cbPage;
    pb = (BYTE *) VirtualAlloc( m_rgItem, m_dbAlloc, MEM_COMMIT, PAGE_READWRITE );
    if (pb == NULL)
        {
        VirtualFree((VOID *) m_rgItem, 0, MEM_RELEASE );
        m_rgItem = NULL;
        return ResultFromScode( E_OUTOFMEMORY );
        }

    m_cbAlloc = m_dbAlloc;
    return ResultFromScode( S_OK );
}
```
範例 Windows GitHub 上的[傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp)。

## <a name="constants"></a>常數


| 常數/值                                                                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**頁面 \_執行**</dt> <dt>0x10</dt> </dl>                                       | 允許對已認可的頁面區域執行存取。 嘗試寫入認可的區域會導致存取違規。<br/> [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數不支援此旗標。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**頁面 \_執行 \_ 讀取**</dt> <dt>0x20</dt> </dl>                       | 允許對已認可的頁面區域執行或唯讀存取。 嘗試寫入認可的區域會導致存取違規。<br/> **Windows Server 2003 和 Windows XP：** 在 Windows XP SP2 和 Windows Server 2003 SP1 之前， [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函式不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**頁面 \_執行 \_ READWRITE**</dt> <dt>0x40</dt> </dl>        | 啟用所認可之頁面區域的執行、唯讀或讀取/寫入存取權。<br/> **Windows Server 2003 和 Windows XP：** 在 Windows XP SP2 和 Windows Server 2003 SP1 之前， [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函式不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**頁面 \_執行 \_ WRITECOPY**</dt> <dt>0x80</dt> </dl>        | 啟用「執行」、「唯讀」或「寫入時寫入」許可權，以存取檔案對應物件的對應視圖。 嘗試寫入已認可的寫入寫入頁面，會導致頁面的私用複本進行處理。 私用頁面會標示為 **page \_ EXECUTE \_ READWRITE**，而變更會寫入至新頁面。<br/> [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)或 [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)函數不支援此旗標。 **Windows Vista、Windows Server 2003 和 Windows XP：** 在 Windows Vista SP1 和 Windows Server 2008 之前， [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函式不支援這個屬性。<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**頁面 \_NOACCESS**</dt> <dt>0x01</dt> </dl>                                    | 停用對已認可之頁面區域的所有存取。 嘗試讀取、寫入或執行認可的區域會導致存取違規。<br/> [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數不支援此旗標。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**頁面 \_READONLY**</dt> <dt>0x02</dt> </dl>                                    | 啟用頁面認可區域的唯讀存取。 嘗試寫入認可的區域會導致存取違規。 如果啟用 [資料執行防止](data-execution-prevention.md) ，嘗試在認可的區域中執行程式碼會造成存取違規。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**頁面 \_READWRITE**</dt> <dt>0x04</dt> </dl>                                 | 啟用已認可之頁面區域的唯讀或讀取/寫入存取。 如果啟用 [資料執行防止](data-execution-prevention.md) ，嘗試在認可的區域中執行程式碼會造成存取違規。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**頁面 \_WRITECOPY**</dt> <dt>0x08</dt> </dl>                                 | 啟用檔案對應物件之對應視圖的唯讀或寫入存取權。 嘗試寫入已認可的寫入寫入頁面，會導致頁面的私用複本進行處理。 私用頁面會標示為 **頁面 \_ READWRITE**，而變更會寫入至新頁面。 如果啟用 [資料執行防止](data-execution-prevention.md) ，嘗試在認可的區域中執行程式碼會造成存取違規。<br/> [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)或 [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)函數不支援此旗標。<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**頁面 \_目標 \_ 無效**</dt>的 <dt>0x40000000</dt> </dl>        | 將頁面中的所有位置設定為 CFG 的無效目標。 搭配任何執行頁面保護（例如 **page \_ execute**、 **page \_ execute \_ READ**、 **page \_ execute \_ READWRITE** 和 **page \_ execute \_ WRITECOPY**）一起使用。 任何間接呼叫這些頁面中的位置都將無法進行 CFG 檢查，而且會終止進程。 所配置之可執行檔頁面的預設行為是標示為 CFG 的有效呼叫目標。<br/> [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)或 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數不支援此旗標。<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**頁面 \_\_無 \_ 更新**</dt> <dt>0x40000000</dt>的目標 </dl> | 在 [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)的保護變更時，區域中的頁面不會更新其 CFG 資訊。 例如，如果區域中的頁面是使用 **\_ \_ 不正確頁面目標** 所配置，則當頁面保護變更時，將會保留不正確資訊。 只有當保護變更為可執行檔類型（例如 **page \_ execute**、 **page \_ execute \_ READ**、 **page \_ execute \_ READWRITE** 和 **page \_ execute \_ WRITECOPY**）時，此旗標才有效。 **VirtualProtect** 保護變更為可執行檔的預設行為是將所有位置標示為 CFG 的有效呼叫目標。 <br/>                                           |



以下是除了先前的表格所提供的選項之外，還可以使用的修飾詞（如所述）。



| 常數/值                                                                                                                                                                                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**頁面 \_GUARD**</dt> <dt>0x100</dt> </dl>                      | 區域中的頁面會變成防護頁面。 任何存取防護頁面的嘗試都會導致系統引發 **狀態 \_ 防護 \_ 頁面 \_ 違規** 例外狀況，並關閉防護頁面狀態。 保護頁面，因此可作為一次性存取警示。 如需詳細資訊，請參閱 [Creating Guard Pages](creating-guard-pages.md) (建立防護頁面)。<br/> 當存取嘗試導致系統關閉防護頁面狀態時，就會接管基礎頁面保護。<br/> 如果在系統服務期間發生防護頁面例外狀況，服務通常會傳回「失敗狀態」指標。<br/> 此值無法搭配 **頁面 \_ NOACCESS** 使用。<br/> [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數不支援此旗標。<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**頁面 \_NOCACHE**</dt> <dt>0x200</dt> </dl>                | 將所有頁面設定為非 cachable。 除非裝置明確需要，否則應用程式不應使用此屬性。 使用連鎖函數搭配與 **SEC \_ NOCACHE** 對應的記憶體，可能會導致例外狀況 **不 \_ 合法的 \_ 指令** 例外狀況。<br/> **頁面 \_ NOCACHE** 旗標不可與 **page \_ GUARD**、 **page \_ NOACCESS** 或 **page \_ WRITECOMBINE** 旗標一起使用。<br/> 只有在使用 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)、 [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)或 [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)函數配置私用記憶體時，才能使用 **頁面 \_ NOCACHE** 旗標。 若要啟用共用記憶體的非快取記憶體存取，請在呼叫 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數時指定 **SEC \_ NOCACHE** 旗標。<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**頁面 \_WRITECOMBINE**</dt> <dt>0x400</dt> </dl> | 將所有頁面設定為寫入組合。 <br/> 除非裝置明確需要，否則應用程式不應使用此屬性。 使用連鎖函數搭配對應為寫入組合的記憶體，可能會導致例外狀況不 **\_ 合法的 \_ 指令** 例外狀況。 <br/> 頁面 **\_ WRITECOMBINE** 旗標無法使用 **頁面 \_ NOACCESS**、 **頁面 \_ 保護** 和 **頁面 \_ NOCACHE** 旗標來指定。 <br/> 只有在使用 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)、 [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)或 [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)函數配置私用記憶體時，才能使用 **頁面 \_ WRITECOMBINE** 旗標。 若要啟用共用記憶體的寫入合併記憶體存取，請在呼叫 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數時指定 **SEC \_ WRITECOMBINE** 旗標。<br/> **Windows Server 2003 和 Windows XP：** 在 Windows Server 2003 SP1 之前，不支援此旗標。<br/> |



當您指定具有 Intel Software Guard Extensions (SGX) 架構的記憶體保護區時，只能搭配 [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) 函數使用下列常數。



| 常數                                                                                                                                                                                                  | 描述                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**頁面 \_ 記憶體保護區 \_ 執行緒 \_ 控制項**</dt> </dl> | 頁面包含 (TCS) 的執行緒控制項結構。<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**頁面 \_ 記憶體保護區 \_ 未經驗證**</dt> </dl>           | 您提供的頁面內容會使用 Intel SGX 程式設計模型的 EEXTEND 指令，從度量中排除。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>WinNT (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)
</dt> <dt>

[記憶體保護](memory-protection.md)
</dt> <dt>

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
</dt> <dt>

[**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)
</dt> <dt>

[**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)
</dt> </dl>

 

 
