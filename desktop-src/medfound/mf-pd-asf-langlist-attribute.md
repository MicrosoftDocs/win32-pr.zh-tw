---
description: 指定語言識別項清單，指定 Advanced Systems 格式所包含的語言 (ASF) 檔。 這個屬性會對應至在 ASF 規格中定義的語言清單物件。
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: 'MF_PD_ASF_LANGLIST 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecac5eac178c7fb315e0ca4cfdbd540a27eeac28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975188"
---
# <a name="mf_pd_asf_langlist-attribute"></a><span data-ttu-id="ffa19-104">MF \_ PD \_ ASF \_ LANGLIST 屬性</span><span class="sxs-lookup"><span data-stu-id="ffa19-104">MF\_PD\_ASF\_LANGLIST attribute</span></span>

<span data-ttu-id="ffa19-105">指定語言識別項清單，指定 Advanced Systems 格式所包含的語言 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="ffa19-105">Specifies a list of language identifiers which specifies the languages contained in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="ffa19-106">這個屬性會對應至在 ASF 規格中定義的語言清單物件。</span><span class="sxs-lookup"><span data-stu-id="ffa19-106">This attribute corresponds to the Language List Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="ffa19-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="ffa19-107">Data type</span></span>

<span data-ttu-id="ffa19-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="ffa19-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="ffa19-109">備註</span><span class="sxs-lookup"><span data-stu-id="ffa19-109">Remarks</span></span>

<span data-ttu-id="ffa19-110">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="ffa19-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="ffa19-111">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從語言清單物件標頭產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ffa19-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Language List Object header.</span></span> <span data-ttu-id="ffa19-112">下表顯示 blob 的格式：</span><span class="sxs-lookup"><span data-stu-id="ffa19-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="ffa19-113">語言清單物件欄位</span><span class="sxs-lookup"><span data-stu-id="ffa19-113">Language List Object field</span></span> | <span data-ttu-id="ffa19-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="ffa19-114">Data type</span></span>    | <span data-ttu-id="ffa19-115">大小</span><span class="sxs-lookup"><span data-stu-id="ffa19-115">Size</span></span>    | <span data-ttu-id="ffa19-116">Description</span><span class="sxs-lookup"><span data-stu-id="ffa19-116">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="ffa19-117">語言識別項記錄計數</span><span class="sxs-lookup"><span data-stu-id="ffa19-117">Language ID Records Count</span></span>  | <span data-ttu-id="ffa19-118">**Dword**</span><span class="sxs-lookup"><span data-stu-id="ffa19-118">**DWORD**</span></span>    | <span data-ttu-id="ffa19-119">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ffa19-119">4 bytes</span></span> | <span data-ttu-id="ffa19-120">語言數目</span><span class="sxs-lookup"><span data-stu-id="ffa19-120">Number of languages</span></span>                    |
| <span data-ttu-id="ffa19-121">語言識別項記錄</span><span class="sxs-lookup"><span data-stu-id="ffa19-121">Language ID Records</span></span>        | <span data-ttu-id="ffa19-122">**位元組**\[\]</span><span class="sxs-lookup"><span data-stu-id="ffa19-122">**BYTE**\[\]</span></span> | <span data-ttu-id="ffa19-123">不定</span><span class="sxs-lookup"><span data-stu-id="ffa19-123">Varies</span></span>  | <span data-ttu-id="ffa19-124">語言字串的陣列 (請參閱下面的) 。</span><span class="sxs-lookup"><span data-stu-id="ffa19-124">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="ffa19-125">第一個 **DWORD** 是語言的數目，後面接著語言識別項字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="ffa19-125">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="ffa19-126">每個字串的格式如下：</span><span class="sxs-lookup"><span data-stu-id="ffa19-126">Each string has the following format:</span></span>



| <span data-ttu-id="ffa19-127">語言清單物件欄位</span><span class="sxs-lookup"><span data-stu-id="ffa19-127">Language List Object field</span></span> | <span data-ttu-id="ffa19-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="ffa19-128">Data type</span></span>     | <span data-ttu-id="ffa19-129">大小</span><span class="sxs-lookup"><span data-stu-id="ffa19-129">Size</span></span>    | <span data-ttu-id="ffa19-130">Description</span><span class="sxs-lookup"><span data-stu-id="ffa19-130">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa19-131">語言識別項長度</span><span class="sxs-lookup"><span data-stu-id="ffa19-131">Language ID Length</span></span>         | <span data-ttu-id="ffa19-132">**Dword**</span><span class="sxs-lookup"><span data-stu-id="ffa19-132">**DWORD**</span></span>     | <span data-ttu-id="ffa19-133">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="ffa19-133">4 bytes</span></span> | <span data-ttu-id="ffa19-134">字串的長度（以位元組為單位），包括尾端 **Null** 字元的大小。</span><span class="sxs-lookup"><span data-stu-id="ffa19-134">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="ffa19-135">語言識別碼</span><span class="sxs-lookup"><span data-stu-id="ffa19-135">Language ID</span></span>                | <span data-ttu-id="ffa19-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="ffa19-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="ffa19-137">不定</span><span class="sxs-lookup"><span data-stu-id="ffa19-137">Varies</span></span>  | <span data-ttu-id="ffa19-138">以 null 終止的字串，包含 RFC 1766 語言名稱。</span><span class="sxs-lookup"><span data-stu-id="ffa19-138">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="ffa19-139">每個字串都是符合 RFC 1766 的語言標記。</span><span class="sxs-lookup"><span data-stu-id="ffa19-139">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="ffa19-140">若要取得 ASF 檔案中特定資料流程的語言標記，請查詢適用于 [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 語言 \_ 識別碼 \_ 索引**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) 屬性的資料流程描述元。</span><span class="sxs-lookup"><span data-stu-id="ffa19-140">To get the language tag for a particular stream in the ASF file, query the stream descriptor for the [**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="ffa19-141">範例</span><span class="sxs-lookup"><span data-stu-id="ffa19-141">Examples</span></span>

<span data-ttu-id="ffa19-142">下列範例顯示如何剖析語言清單。</span><span class="sxs-lookup"><span data-stu-id="ffa19-142">The following example shows how to parse the language list.</span></span>


```C++
class LanguageList
{
private:
    UINT8   *pRawList;          // Unparsed blob
    UINT32  cbList;             // Size of the blob, in bytes
    DWORD   cLangs;             // Number of languages
    WCHAR   **ppszLanguages;    // Array of pointers to strings.
                                // These are pointers into pRawList.
public:
    LanguageList() : 
        pRawList(NULL), cbList(0), ppszLanguages(NULL), cLangs(0)
    {
    }
    ~LanguageList()
    {
        Clear();
    }

    // Clear: Clears the list.
    void Clear()
    {
        CoTaskMemFree(pRawList);
        cbList = 0;
        cLangs = 0;
        delete [] ppszLanguages;

        ppszLanguages = NULL;
    }

    // GetCount: Returns the number of languages.
    DWORD GetCount() const { return cLangs; }

    // GetLanguage: Return the i'th string in the list.
    const WCHAR* GetLanguage(DWORD i)
    {
        if (i >= cLangs)
        {
            return NULL;
        }
        return ppszLanguages[i];
    }

    // Initialize: Get the language list, if specified, and parse it.
    HRESULT Initialize(IMFPresentationDescriptor *pPD)
    {
        if (pPD == NULL)
        {
            return E_POINTER;
        }
        Clear();

        HRESULT hr = pPD->GetAllocatedBlob(
            MF_PD_ASF_LANGLIST, &pRawList, &cbList);

        if (FAILED(hr))
        {
            goto done;
        }


        // Parse the language blob.

        // Record count.
        if (cbList < sizeof(DWORD))
        {
            hr = E_FAIL;
            goto done;
        }

        cLangs = ((DWORD*)pRawList)[0];

        // Allocate an array of pointers to language strings.
        ppszLanguages = new (std::nothrow) WCHAR*[cLangs];
        if (ppszLanguages == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        ZeroMemory(ppszLanguages, cLangs * sizeof(WCHAR*));

        BYTE *pNext = pRawList + sizeof(DWORD); // Next byte.
        BYTE *pEnd = pRawList + cbList;         // End of the blob.

        for (DWORD i = 0; i < cLangs; i++)
        {
            if (pNext > pEnd - sizeof(DWORD))
            {
                hr = E_FAIL;
                goto done;
            }

            // Language ID length
            DWORD cbStr = ((DWORD*)pNext)[0];
            pNext += sizeof(DWORD);

            // Calculate the pointer to the language ID string.
            if ((cbStr > (size_t)(pEnd - pNext)) ||
                (cbStr < sizeof(WCHAR)) || 
                (cbStr % sizeof(WCHAR) != 0))
            {
                hr = E_FAIL;
                goto done;
            }

            ppszLanguages[i] = (WCHAR*)pNext;

            // Verify the string is NULL-terminated.
            if (ppszLanguages[i][(cbStr / sizeof(WCHAR)) - 1] != L'\0')
            {
                hr = E_FAIL;
                goto done;
            }
            pNext += cbStr;
        }

done:
        if (FAILED(hr))
        {
            Clear();
        }

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // There was no language list attribute in the PD.
            // This is not a failure case.
            hr = S_OK;  
        }
        return hr;
    }

private:
    LanguageList(const LanguageList& lang);
    LanguageList& operator=(const LanguageList& lang);
};
```



## <a name="requirements"></a><span data-ttu-id="ffa19-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffa19-143">Requirements</span></span>



| <span data-ttu-id="ffa19-144">需求</span><span class="sxs-lookup"><span data-stu-id="ffa19-144">Requirement</span></span> | <span data-ttu-id="ffa19-145">值</span><span class="sxs-lookup"><span data-stu-id="ffa19-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa19-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffa19-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa19-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffa19-147">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ffa19-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffa19-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa19-149">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffa19-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ffa19-150">標頭</span><span class="sxs-lookup"><span data-stu-id="ffa19-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffa19-151"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="ffa19-151"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffa19-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffa19-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa19-153">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ffa19-153">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ffa19-154">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="ffa19-154">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="ffa19-155">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="ffa19-155">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="ffa19-156">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ffa19-156">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ffa19-157">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="ffa19-157">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="ffa19-158">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="ffa19-158">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="ffa19-159">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="ffa19-159">ASF Header Object</span></span>
</dt> <dt>

[<span data-ttu-id="ffa19-160">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="ffa19-160">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




