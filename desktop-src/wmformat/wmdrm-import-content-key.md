---
title: 'WMDRM_IMPORT_CONTENT_KEY 結構 (Drmexternals .h) '
description: WMDRM 匯 \_ 入 \_ 內容 \_ 金鑰結構會儲存匯入受保護內容時所使用的內容金鑰。
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- WMDRM_IMPORT_CONTENT_KEY 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383990"
---
# <a name="wmdrm_import_content_key-structure"></a><span data-ttu-id="7eaed-105">WMDRM 匯 \_ 入 \_ 內容 \_ 金鑰結構</span><span class="sxs-lookup"><span data-stu-id="7eaed-105">WMDRM\_IMPORT\_CONTENT\_KEY structure</span></span>

<span data-ttu-id="7eaed-106">**WMDRM 匯 \_ 入 \_ 內容 \_ 金鑰** 結構會儲存匯入受保護內容時所使用的內容金鑰。</span><span class="sxs-lookup"><span data-stu-id="7eaed-106">The **WMDRM\_IMPORT\_CONTENT\_KEY** structure stores the content key used in importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eaed-107">語法</span><span class="sxs-lookup"><span data-stu-id="7eaed-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a><span data-ttu-id="7eaed-108">成員</span><span class="sxs-lookup"><span data-stu-id="7eaed-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7eaed-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="7eaed-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7eaed-110">版本。</span><span class="sxs-lookup"><span data-stu-id="7eaed-110">Version.</span></span>

</dd> <dt>

<span data-ttu-id="7eaed-111">**cbStructSize**</span><span class="sxs-lookup"><span data-stu-id="7eaed-111">**cbStructSize**</span></span>
</dt> <dd>

<span data-ttu-id="7eaed-112">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7eaed-112">Size of structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7eaed-113">**dwIVKeyType**</span><span class="sxs-lookup"><span data-stu-id="7eaed-113">**dwIVKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="7eaed-114">初始化向量索引鍵類型。</span><span class="sxs-lookup"><span data-stu-id="7eaed-114">Initialization vector key type.</span></span> <span data-ttu-id="7eaed-115">設定為 WMDRM \_ KEYTYPE \_ RC4。</span><span class="sxs-lookup"><span data-stu-id="7eaed-115">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="7eaed-116">**cbIVKey**</span><span class="sxs-lookup"><span data-stu-id="7eaed-116">**cbIVKey**</span></span>
</dt> <dd>

<span data-ttu-id="7eaed-117">初始化向量索引鍵的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7eaed-117">Size of the initialization vector key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7eaed-118">**dwContentKeyType**</span><span class="sxs-lookup"><span data-stu-id="7eaed-118">**dwContentKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="7eaed-119">內容金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="7eaed-119">Content key type.</span></span> <span data-ttu-id="7eaed-120">設定為 WMDRM \_ KEYTYPE \_ 雞尾酒。</span><span class="sxs-lookup"><span data-stu-id="7eaed-120">Set to WMDRM\_KEYTYPE\_COCKTAIL.</span></span>

</dd> <dt>

<span data-ttu-id="7eaed-121">**cbContentKey**</span><span class="sxs-lookup"><span data-stu-id="7eaed-121">**cbContentKey**</span></span>
</dt> <dd>

<span data-ttu-id="7eaed-122">內容金鑰的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7eaed-122">Size of the content key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7eaed-123">**rgbKeyData**</span><span class="sxs-lookup"><span data-stu-id="7eaed-123">**rgbKeyData**</span></span>
</dt> <dd>

<span data-ttu-id="7eaed-124">包含內容索引鍵的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="7eaed-124">Address of a buffer containing the content key.</span></span> <span data-ttu-id="7eaed-125">緩衝區大小必須符合 **cbContentKey** 的值。</span><span class="sxs-lookup"><span data-stu-id="7eaed-125">The buffer size must match the value of **cbContentKey**.</span></span> <span data-ttu-id="7eaed-126">此金鑰應符合從 XMR 授權訊息匯入的金鑰。</span><span class="sxs-lookup"><span data-stu-id="7eaed-126">This key should match the key imported from the XMR license message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7eaed-127">備註</span><span class="sxs-lookup"><span data-stu-id="7eaed-127">Remarks</span></span>

<span data-ttu-id="7eaed-128">此結構（包括包含工作階段金鑰的緩衝區）必須使用工作階段金鑰進行加密，並包含在 [**WMDRM 匯 \_ 入 \_ INIT \_ 結構**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)結構的 **pbEncryptedKeyMessage** 成員中。</span><span class="sxs-lookup"><span data-stu-id="7eaed-128">This structure, including the buffer containing the session key, must be encrypted with the session key and included in the **pbEncryptedKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eaed-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="7eaed-129">Requirements</span></span>



| <span data-ttu-id="7eaed-130">需求</span><span class="sxs-lookup"><span data-stu-id="7eaed-130">Requirement</span></span> | <span data-ttu-id="7eaed-131">值</span><span class="sxs-lookup"><span data-stu-id="7eaed-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eaed-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7eaed-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7eaed-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7eaed-133">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7eaed-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7eaed-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7eaed-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7eaed-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7eaed-136">版本</span><span class="sxs-lookup"><span data-stu-id="7eaed-136">Version</span></span><br/>                  | <span data-ttu-id="7eaed-137">Windows Media Format 11 SDK</span><span class="sxs-lookup"><span data-stu-id="7eaed-137">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="7eaed-138">標頭</span><span class="sxs-lookup"><span data-stu-id="7eaed-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7eaed-139"><dt>Drmexternals。h</dt></span><span class="sxs-lookup"><span data-stu-id="7eaed-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eaed-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7eaed-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eaed-141">**結構**</span><span class="sxs-lookup"><span data-stu-id="7eaed-141">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





