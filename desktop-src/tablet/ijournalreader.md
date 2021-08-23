---
description: 提供對 Windows 筆記本檔案的讀取權限，並傳回包含檔案內容之 XML 版本的資料流程。
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: 'IJournalReader 介面 (日記 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: ff0151432e38a3e611e09efe2d5192eefb8c1d3e6cb0e79296e992b728c5a16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590309"
---
# <a name="ijournalreader-interface"></a>IJournalReader 介面

提供對 Windows 筆記本檔案的讀取權限，並傳回包含檔案內容之 XML 版本的資料流程。

> [!Note]  
> 日誌讀取器元件無法讀取執行 Windows 7 或更新版本的電腦所建立的 Windows 筆記本檔案。 IJournalReader 介面應視為已淘汰或已淘汰，不應該使用。

 

## <a name="members"></a>成員

**IJournalReader** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IJournalReader** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IJournalReader** 介面具有這些方法。



| 方法                                                  | 描述                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**ReadFromStream**](ijournalreader-readfromstream.md) | 將資料流程帶到筆記本便箋檔案，並傳回代表檔內容的 XML 資料流程。<br/> |



 

## <a name="remarks"></a>備註

**JournalReader** 類別可讓您載入日誌檔串流，以及接收代表內容的 XML 資料流程。 您可以重建、顯示及操作筆墨。

## <a name="examples"></a>範例

下列按鈕的 [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) 事件處理常式範例會建立 **JournalReader** 類別的實例，並使用它來讀取現有的日誌檔案。

> [!Note]  
> 不會顯示從此範例呼叫的 **DisplayXml** 方法。 這種方法的特定執行取決於您應用程式的需求。

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
  }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                         |
| 標頭<br/>                   | <dl> <dt>.H (也需要日記 \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[自訂屬性 Guid](custom-property-guids.md)
</dt> <dt>

[**ReadFromStream 方法**](ijournalreader-readfromstream.md)
</dt> </dl>

 

