---
title: 'WMDRM_IMPORT_SESSION_KEY 結構 (Drmexternals .h) '
description: WMDRM 匯 \_ 入 \_ 會話 \_ 金鑰結構會保存用來匯入受保護內容的工作階段金鑰。
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105305"
---
# <a name="wmdrm_import_session_key-structure"></a><span data-ttu-id="d1fb7-105">WMDRM 匯 \_ 入 \_ 會話 \_ 金鑰結構</span><span class="sxs-lookup"><span data-stu-id="d1fb7-105">WMDRM\_IMPORT\_SESSION\_KEY structure</span></span>

<span data-ttu-id="d1fb7-106">**WMDRM 匯 \_ 入 \_ 會話 \_ 金鑰** 結構會保存用來匯入受保護內容的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="d1fb7-106">The **WMDRM\_IMPORT\_SESSION\_KEY** structure holds the session key for importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1fb7-107">語法</span><span class="sxs-lookup"><span data-stu-id="d1fb7-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a><span data-ttu-id="d1fb7-108">成員</span><span class="sxs-lookup"><span data-stu-id="d1fb7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1fb7-109">**dwKeyType**</span><span class="sxs-lookup"><span data-stu-id="d1fb7-109">**dwKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="d1fb7-110">工作階段金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="d1fb7-110">Session key type.</span></span> <span data-ttu-id="d1fb7-111">設定為 WMDRM \_ KEYTYPE \_ RC4。</span><span class="sxs-lookup"><span data-stu-id="d1fb7-111">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="d1fb7-112">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="d1fb7-112">**cbKey**</span></span>
</dt> <dd>

<span data-ttu-id="d1fb7-113">工作階段金鑰的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d1fb7-113">Size of the session key, in bytes.</span></span> <span data-ttu-id="d1fb7-114">此值可以是您所需的最大值，因為對整個訊息的單一 RSA OAEP 作業限制 (此結構以及工作階段金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="d1fb7-114">This value can be as large as you need, given the limits of a single RSA OAEP operation over the entire message (this structure plus the session key).</span></span>

</dd> <dt>

<span data-ttu-id="d1fb7-115">**rgbKey**</span><span class="sxs-lookup"><span data-stu-id="d1fb7-115">**rgbKey**</span></span>
</dt> <dd>

<span data-ttu-id="d1fb7-116">包含工作階段金鑰之緩衝區的位址。</span><span class="sxs-lookup"><span data-stu-id="d1fb7-116">Address of a buffer containing the session key.</span></span> <span data-ttu-id="d1fb7-117">緩衝區大小必須符合 **cbKey** 的值。</span><span class="sxs-lookup"><span data-stu-id="d1fb7-117">The buffer size must match the value of **cbKey**.</span></span> <span data-ttu-id="d1fb7-118">緩衝區中的資料是隨機產生的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="d1fb7-118">The data in the buffer is a randomly generated key value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1fb7-119">備註</span><span class="sxs-lookup"><span data-stu-id="d1fb7-119">Remarks</span></span>

<span data-ttu-id="d1fb7-120">此結構（包括包含工作階段金鑰的緩衝區）必須使用 Windows Media DRM 電腦公開金鑰進行加密，並包含在 [**WMDRM 匯 \_ 入 \_ INIT \_ 結構**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)結構的 **pbEncryptedSessionKeyMessage** 成員中。</span><span class="sxs-lookup"><span data-stu-id="d1fb7-120">This structure, including the buffer containing the session key, must be encrypted with the Windows Media DRM machine public key and included in the **pbEncryptedSessionKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1fb7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1fb7-121">Requirements</span></span>



| <span data-ttu-id="d1fb7-122">需求</span><span class="sxs-lookup"><span data-stu-id="d1fb7-122">Requirement</span></span> | <span data-ttu-id="d1fb7-123">值</span><span class="sxs-lookup"><span data-stu-id="d1fb7-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1fb7-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1fb7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1fb7-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1fb7-125">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d1fb7-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1fb7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1fb7-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1fb7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d1fb7-128">版本</span><span class="sxs-lookup"><span data-stu-id="d1fb7-128">Version</span></span><br/>                  | <span data-ttu-id="d1fb7-129">Windows Media Format 11 SDK</span><span class="sxs-lookup"><span data-stu-id="d1fb7-129">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="d1fb7-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d1fb7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1fb7-131"><dt>Drmexternals。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1fb7-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1fb7-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1fb7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1fb7-133">**結構**</span><span class="sxs-lookup"><span data-stu-id="d1fb7-133">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





