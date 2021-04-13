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
ms.openlocfilehash: 7576996d341f13518879310f08c0a48996e1293f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320940"
---
# <a name="ijournalreader-interface"></a><span data-ttu-id="15406-103">IJournalReader 介面</span><span class="sxs-lookup"><span data-stu-id="15406-103">IJournalReader interface</span></span>

<span data-ttu-id="15406-104">提供對 Windows 筆記本檔案的讀取權限，並傳回包含檔案內容之 XML 版本的資料流程。</span><span class="sxs-lookup"><span data-stu-id="15406-104">Provides read access to a Windows Journal file, returning a stream containing an XML version of the file's contents.</span></span>

> [!Note]  
> <span data-ttu-id="15406-105">日誌讀取器元件無法讀取執行 Windows 7 或更新版本的電腦所建立的 Windows 筆記本檔案。</span><span class="sxs-lookup"><span data-stu-id="15406-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="15406-106">IJournalReader 介面應視為已淘汰或已淘汰，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="15406-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="members"></a><span data-ttu-id="15406-107">成員</span><span class="sxs-lookup"><span data-stu-id="15406-107">Members</span></span>

<span data-ttu-id="15406-108">**IJournalReader** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="15406-108">The **IJournalReader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="15406-109">**IJournalReader** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="15406-109">**IJournalReader** also has these types of members:</span></span>

-   [<span data-ttu-id="15406-110">方法</span><span class="sxs-lookup"><span data-stu-id="15406-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="15406-111">方法</span><span class="sxs-lookup"><span data-stu-id="15406-111">Methods</span></span>

<span data-ttu-id="15406-112">**IJournalReader** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="15406-112">The **IJournalReader** interface has these methods.</span></span>



| <span data-ttu-id="15406-113">方法</span><span class="sxs-lookup"><span data-stu-id="15406-113">Method</span></span>                                                  | <span data-ttu-id="15406-114">描述</span><span class="sxs-lookup"><span data-stu-id="15406-114">Description</span></span>                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15406-115">**ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="15406-115">**ReadFromStream**</span></span>](ijournalreader-readfromstream.md) | <span data-ttu-id="15406-116">將資料流程帶到筆記本便箋檔案，並傳回代表檔內容的 XML 資料流程。</span><span class="sxs-lookup"><span data-stu-id="15406-116">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="15406-117">備註</span><span class="sxs-lookup"><span data-stu-id="15406-117">Remarks</span></span>

<span data-ttu-id="15406-118">**JournalReader** 類別可讓您載入日誌檔串流，以及接收代表內容的 XML 資料流程。</span><span class="sxs-lookup"><span data-stu-id="15406-118">The **JournalReader** class enables you to load a Journal document stream and to receive an XML stream representing the contents.</span></span> <span data-ttu-id="15406-119">您可以重建、顯示及操作筆墨。</span><span class="sxs-lookup"><span data-stu-id="15406-119">You can reconstitute, display, and manipulate the ink.</span></span>

## <a name="examples"></a><span data-ttu-id="15406-120">範例</span><span class="sxs-lookup"><span data-stu-id="15406-120">Examples</span></span>

<span data-ttu-id="15406-121">下列按鈕的 [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) 事件處理常式範例會建立 **JournalReader** 類別的實例，並使用它來讀取現有的日誌檔案。</span><span class="sxs-lookup"><span data-stu-id="15406-121">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the **JournalReader** class and uses it to read an existing Journal file.</span></span>

> [!Note]  
> <span data-ttu-id="15406-122">不會顯示從此範例呼叫的 **DisplayXml** 方法。</span><span class="sxs-lookup"><span data-stu-id="15406-122">The **DisplayXml** method called from this example is not shown.</span></span> <span data-ttu-id="15406-123">這種方法的特定執行取決於您應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="15406-123">The specific implementation of such a method is dependent on your application's needs.</span></span>

 


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



## <a name="requirements"></a><span data-ttu-id="15406-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="15406-124">Requirements</span></span>



| <span data-ttu-id="15406-125">需求</span><span class="sxs-lookup"><span data-stu-id="15406-125">Requirement</span></span> | <span data-ttu-id="15406-126">值</span><span class="sxs-lookup"><span data-stu-id="15406-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15406-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15406-127">Minimum supported client</span></span><br/> | <span data-ttu-id="15406-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15406-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15406-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15406-129">Minimum supported server</span></span><br/> | <span data-ttu-id="15406-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="15406-130">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="15406-131">標頭</span><span class="sxs-lookup"><span data-stu-id="15406-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="15406-132"><dt>.H (也需要日記 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="15406-132"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="15406-133">DLL</span><span class="sxs-lookup"><span data-stu-id="15406-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15406-134"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15406-134"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="15406-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15406-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15406-136">自訂屬性 Guid</span><span class="sxs-lookup"><span data-stu-id="15406-136">Custom Property GUIDs</span></span>](custom-property-guids.md)
</dt> <dt>

[<span data-ttu-id="15406-137">**ReadFromStream 方法**</span><span class="sxs-lookup"><span data-stu-id="15406-137">**ReadFromStream Method**</span></span>](ijournalreader-readfromstream.md)
</dt> </dl>

 

