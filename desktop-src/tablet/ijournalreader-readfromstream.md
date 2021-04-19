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
ms.openlocfilehash: 258ac30b8857fa4ef24bd86a08c7e402229f4bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966679"
---
# <a name="ijournalreaderreadfromstream-method"></a><span data-ttu-id="81fd3-103">IJournalReader：： ReadFromStream 方法</span><span class="sxs-lookup"><span data-stu-id="81fd3-103">IJournalReader::ReadFromStream method</span></span>

<span data-ttu-id="81fd3-104">將資料流程帶到筆記本便箋檔案，並傳回代表檔內容的 XML 資料流程。</span><span class="sxs-lookup"><span data-stu-id="81fd3-104">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span>

> [!Note]  
> <span data-ttu-id="81fd3-105">日誌讀取器元件無法讀取執行 Windows 7 或更新版本的電腦所建立的 Windows 筆記本檔案。</span><span class="sxs-lookup"><span data-stu-id="81fd3-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="81fd3-106">IJournalReader 介面應視為已淘汰或已淘汰，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="81fd3-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="81fd3-107">語法</span><span class="sxs-lookup"><span data-stu-id="81fd3-107">Syntax</span></span>


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a><span data-ttu-id="81fd3-108">參數</span><span class="sxs-lookup"><span data-stu-id="81fd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81fd3-109">*pJournalFileStream* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81fd3-109">*pJournalFileStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81fd3-110">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)物件，代表要讀取的日誌檔案。</span><span class="sxs-lookup"><span data-stu-id="81fd3-110">An [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object representing the Journal file to read.</span></span>

</dd> <dt>

<span data-ttu-id="81fd3-111">*ppXmlStream* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="81fd3-111">*ppXmlStream* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="81fd3-112">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)物件位址的指標，該物件會接收藉由讀取日誌檔案所建立的 XML 資料流程。</span><span class="sxs-lookup"><span data-stu-id="81fd3-112">A pointer to the address of an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object that will receive the XML stream created by reading the Journal file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81fd3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="81fd3-113">Return value</span></span>

<span data-ttu-id="81fd3-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="81fd3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81fd3-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="81fd3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81fd3-116">備註</span><span class="sxs-lookup"><span data-stu-id="81fd3-116">Remarks</span></span>

<span data-ttu-id="81fd3-117">資料流程是用來避免直接存取檔案系統，並允許選擇要使用的 XML 剖析方法。</span><span class="sxs-lookup"><span data-stu-id="81fd3-117">Streams are used to avoid direct access to the file system and to allow choice in which XML parsing method to use.</span></span>

## <a name="examples"></a><span data-ttu-id="81fd3-118">範例</span><span class="sxs-lookup"><span data-stu-id="81fd3-118">Examples</span></span>

<span data-ttu-id="81fd3-119">下列按鈕的 [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) 事件處理常式範例會建立 [**IJournalReader 介面**](ijournalreader.md) 介面的實例，並使用它來讀取現有的日誌檔案。</span><span class="sxs-lookup"><span data-stu-id="81fd3-119">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the [**IJournalReader Interface**](ijournalreader.md) interface and uses it to read an existing Journal file.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="81fd3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="81fd3-120">Requirements</span></span>



| <span data-ttu-id="81fd3-121">需求</span><span class="sxs-lookup"><span data-stu-id="81fd3-121">Requirement</span></span> | <span data-ttu-id="81fd3-122">值</span><span class="sxs-lookup"><span data-stu-id="81fd3-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fd3-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81fd3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="81fd3-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81fd3-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81fd3-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81fd3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="81fd3-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="81fd3-126">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="81fd3-127">標頭</span><span class="sxs-lookup"><span data-stu-id="81fd3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="81fd3-128"><dt>.H (也需要日記 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="81fd3-128"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="81fd3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="81fd3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81fd3-130"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81fd3-130"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="81fd3-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81fd3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81fd3-132">**IJournalReader 介面**</span><span class="sxs-lookup"><span data-stu-id="81fd3-132">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="81fd3-133">日誌讀取器架構參考</span><span class="sxs-lookup"><span data-stu-id="81fd3-133">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

