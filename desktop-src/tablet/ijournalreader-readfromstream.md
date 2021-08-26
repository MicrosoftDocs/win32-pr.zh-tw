---
description: 將資料流程帶到筆記本便箋檔案，並傳回代表檔內容的 XML 資料流程。
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: 'IJournalReader：： ReadFromStream 方法 (日記 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 7dbe9d7929f616914d06cad237f486677cd8e5616cb04bf28a5836751ca0a3c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057848"
---
# <a name="ijournalreaderreadfromstream-method"></a>IJournalReader：： ReadFromStream 方法

將資料流程帶到筆記本便箋檔案，並傳回代表檔內容的 XML 資料流程。

> [!Note]  
> 日誌讀取器元件無法讀取執行 Windows 7 或更新版本的電腦所建立的 Windows 筆記本檔案。 IJournalReader 介面應視為已淘汰或已淘汰，不應該使用。

 

## <a name="syntax"></a>語法


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pJournalFileStream* \[在\]
</dt> <dd>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)物件，代表要讀取的日誌檔案。

</dd> <dt>

*ppXmlStream* \[退出，retval\]
</dt> <dd>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)物件位址的指標，該物件會接收藉由讀取日誌檔案所建立的 XML 資料流程。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

資料流程是用來避免直接存取檔案系統，並允許選擇要使用的 XML 剖析方法。

## <a name="examples"></a>範例

下列按鈕的 [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) 事件處理常式範例會建立 [**IJournalReader 介面**](ijournalreader.md) 介面的實例，並使用它來讀取現有的日誌檔案。


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
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
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
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

[**IJournalReader 介面**](ijournalreader.md)
</dt> <dt>

[日誌讀取器架構參考](journal-reader-schema-reference.md)
</dt> </dl>

 

