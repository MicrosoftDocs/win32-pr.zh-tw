---
description: 包含智慧卡密碼編譯服務提供者 (CSP) 的相關資訊。
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: KERB_SMARTCARD_CSP_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992049"
---
# <a name="kerb_smartcard_csp_info-structure"></a><span data-ttu-id="776e5-103">KERB \_ 智慧卡 \_ CSP \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="776e5-103">KERB\_SMARTCARD\_CSP\_INFO structure</span></span>

<span data-ttu-id="776e5-104">**KERB \_ 智慧卡 \_ CSP \_ 資訊** 結構包含智慧卡 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="776e5-104">The **KERB\_SMARTCARD\_CSP\_INFO** structure contains information about a smart card [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="776e5-105">未在公用標頭中宣告此結構。</span><span class="sxs-lookup"><span data-stu-id="776e5-105">This structure is not declared in a public header.</span></span>

## <a name="syntax"></a><span data-ttu-id="776e5-106">語法</span><span class="sxs-lookup"><span data-stu-id="776e5-106">Syntax</span></span>


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a><span data-ttu-id="776e5-107">成員</span><span class="sxs-lookup"><span data-stu-id="776e5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="776e5-108">**dwCspInfoLen**</span><span class="sxs-lookup"><span data-stu-id="776e5-108">**dwCspInfoLen**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-109">此結構的大小（以位元組為單位），包括任何附加的資料。</span><span class="sxs-lookup"><span data-stu-id="776e5-109">The size, in bytes, of this structure, including any appended data.</span></span>

</dd> <dt>

<span data-ttu-id="776e5-110">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="776e5-110">**MessageType**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-111">傳遞的訊息類型。</span><span class="sxs-lookup"><span data-stu-id="776e5-111">The type of message being passed.</span></span> <span data-ttu-id="776e5-112">此成員必須設定為1。</span><span class="sxs-lookup"><span data-stu-id="776e5-112">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="776e5-113">**CoNtextInformation**</span><span class="sxs-lookup"><span data-stu-id="776e5-113">**ContextInformation**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="776e5-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="776e5-115">**SpaceHolderForWow64**</span><span class="sxs-lookup"><span data-stu-id="776e5-115">**SpaceHolderForWow64**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="776e5-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="776e5-117">**flags**</span><span class="sxs-lookup"><span data-stu-id="776e5-117">**flags**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-118">保留的。</span><span class="sxs-lookup"><span data-stu-id="776e5-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="776e5-119">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="776e5-119">**KeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-120">要從緩衝區 **bBuffer** 內指定的金鑰容器使用的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="776e5-120">The private key to use from the key container specified within the buffer **bBuffer**.</span></span> <span data-ttu-id="776e5-121">索引鍵可以是下列其中一個值，定義于 WinCrypt 中。</span><span class="sxs-lookup"><span data-stu-id="776e5-121">The key can be one of the following values, defined in WinCrypt.h.</span></span>



| <span data-ttu-id="776e5-122">值</span><span class="sxs-lookup"><span data-stu-id="776e5-122">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="776e5-123">意義</span><span class="sxs-lookup"><span data-stu-id="776e5-123">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="776e5-124"><dt>**AT \_KEYEXCHANGE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="776e5-124"><dt>**AT\_KEYEXCHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="776e5-125">金鑰是金鑰交換金鑰。</span><span class="sxs-lookup"><span data-stu-id="776e5-125">The key is a key-exchange key.</span></span><br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="776e5-126"><dt>**AT \_簽名**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="776e5-126"><dt>**AT\_SIGNATURE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="776e5-127">機碼是簽章金鑰。</span><span class="sxs-lookup"><span data-stu-id="776e5-127">The key is a signature key.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="776e5-128">**nCardNameOffset**</span><span class="sxs-lookup"><span data-stu-id="776e5-128">**nCardNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-129">**BBuffer** 緩衝區中的字元數，在該緩衝區中的智慧卡名稱之前。</span><span class="sxs-lookup"><span data-stu-id="776e5-129">The number of characters in the **bBuffer** buffer that precede the name of the smart card in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="776e5-130">如果未提供智慧卡的名稱，緩衝區必須包含空字串。</span><span class="sxs-lookup"><span data-stu-id="776e5-130">If the name of the smart card is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="776e5-131">**nReaderNameOffset**</span><span class="sxs-lookup"><span data-stu-id="776e5-131">**nReaderNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-132">**BBuffer** 緩衝區中的字元數，在該緩衝區中的智慧卡讀取器名稱前面。</span><span class="sxs-lookup"><span data-stu-id="776e5-132">The number of characters in the **bBuffer** buffer that precede the name of the smart card reader in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="776e5-133">如果未提供智慧卡讀卡機的名稱，則緩衝區必須包含空字串。</span><span class="sxs-lookup"><span data-stu-id="776e5-133">If the name of the smart card reader is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="776e5-134">**nContainerNameOffset**</span><span class="sxs-lookup"><span data-stu-id="776e5-134">**nContainerNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-135">**BBuffer** 緩衝區中的字元數，在該緩衝區中的金鑰容器名稱之前。</span><span class="sxs-lookup"><span data-stu-id="776e5-135">The number of characters in the **bBuffer** buffer that precede the name of the key container in that buffer.</span></span> <span data-ttu-id="776e5-136">這個字串不可以是空的。</span><span class="sxs-lookup"><span data-stu-id="776e5-136">This string cannot be empty.</span></span>

</dd> <dt>

<span data-ttu-id="776e5-137">**nCSPNameOffset**</span><span class="sxs-lookup"><span data-stu-id="776e5-137">**nCSPNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-138">**BBuffer** 緩衝區中的字元數，在該緩衝區中的 CSP 名稱之前。</span><span class="sxs-lookup"><span data-stu-id="776e5-138">The number of characters in the **bBuffer** buffer that precede the name of the CSP in that buffer.</span></span>

</dd> <dt>

<span data-ttu-id="776e5-139">**bBuffer**</span><span class="sxs-lookup"><span data-stu-id="776e5-139">**bBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="776e5-140">初始化為長度的字元陣列 `sizeof(DWORD)` 。</span><span class="sxs-lookup"><span data-stu-id="776e5-140">An array of characters initialized to a length of `sizeof(DWORD)`.</span></span> <span data-ttu-id="776e5-141">此緩衝區包含 **nCardNameOffset**、 **nReaderNameOffset**、 **nContainerNameOffset** 和 **nCSPNameOffset** 成員所參考的名稱，以及 CSP 所提供的任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="776e5-141">This buffer contains the names referred to by the **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset**, and **nCSPNameOffset** members, as well as any additional data provided by the CSP.</span></span>

<span data-ttu-id="776e5-142">任何未提供的名稱都必須以空字串在此緩衝區中表示。</span><span class="sxs-lookup"><span data-stu-id="776e5-142">Any names that are not provided must be represented in this buffer by empty strings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="776e5-143">備註</span><span class="sxs-lookup"><span data-stu-id="776e5-143">Remarks</span></span>

<span data-ttu-id="776e5-144">當此結構序列化時，結構成員必須對齊為2個位元組的倍數的界限。</span><span class="sxs-lookup"><span data-stu-id="776e5-144">When this structure is serialized, the structure members must be aligned to boundaries that are multiples of 2 bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="776e5-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="776e5-145">Requirements</span></span>



| <span data-ttu-id="776e5-146">需求</span><span class="sxs-lookup"><span data-stu-id="776e5-146">Requirement</span></span> | <span data-ttu-id="776e5-147">值</span><span class="sxs-lookup"><span data-stu-id="776e5-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="776e5-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="776e5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="776e5-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="776e5-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="776e5-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="776e5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="776e5-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="776e5-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="776e5-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="776e5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776e5-153">**KERB \_ 憑證 \_ 登入**</span><span class="sxs-lookup"><span data-stu-id="776e5-153">**KERB\_CERTIFICATE\_LOGON**</span></span>](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
