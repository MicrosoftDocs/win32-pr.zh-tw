---
description: 定義要在 Microsoft Authenticode 驗證專案資料時使用的資料。
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: 'PST_AUTHENTICODEDATA 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990213"
---
# <a name="pst_authenticodedata-structure"></a><span data-ttu-id="dfd03-103">PST \_ AUTHENTICODEDATA 結構</span><span class="sxs-lookup"><span data-stu-id="dfd03-103">PST\_AUTHENTICODEDATA structure</span></span>

<span data-ttu-id="dfd03-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="dfd03-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="dfd03-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="dfd03-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="dfd03-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="dfd03-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="dfd03-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="dfd03-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="dfd03-108">定義要在 Microsoft Authenticode 驗證專案資料時使用的資料。</span><span class="sxs-lookup"><span data-stu-id="dfd03-108">Defines data to be used in Microsoft Authenticode verification of item data.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd03-109">語法</span><span class="sxs-lookup"><span data-stu-id="dfd03-109">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a><span data-ttu-id="dfd03-110">成員</span><span class="sxs-lookup"><span data-stu-id="dfd03-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="dfd03-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="dfd03-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="dfd03-112">此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="dfd03-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="dfd03-113">**dwModifiers**</span><span class="sxs-lookup"><span data-stu-id="dfd03-113">**dwModifiers**</span></span>
</dt> <dd>

<span data-ttu-id="dfd03-114">值，這個值會識別其中一個呼叫端必須驗證的修飾詞。</span><span class="sxs-lookup"><span data-stu-id="dfd03-114">A value that identifies the modifier that one of a chain of callers must verify.</span></span>



| <span data-ttu-id="dfd03-115">值</span><span class="sxs-lookup"><span data-stu-id="dfd03-115">Value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="dfd03-116">意義</span><span class="sxs-lookup"><span data-stu-id="dfd03-116">Meaning</span></span>                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <span data-ttu-id="dfd03-117"><dt>**PST \_AC \_ 單一 \_ 呼叫者**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dfd03-117"><dt>**PST\_AC\_SINGLE\_CALLER**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="dfd03-118">只有一個層級會在呼叫鏈中 PStore。</span><span class="sxs-lookup"><span data-stu-id="dfd03-118">Only a single level in the call chain to PStore.</span></span> <span data-ttu-id="dfd03-119">呼叫端會通過驗證檢查。</span><span class="sxs-lookup"><span data-stu-id="dfd03-119">The caller passes the verification check.</span></span> <span data-ttu-id="dfd03-120">指定的影像是立即呼叫端，而是應用程式 ( .exe) 。</span><span class="sxs-lookup"><span data-stu-id="dfd03-120">The specified image is the immediate caller, and is an application (.exe).</span></span><br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <span data-ttu-id="dfd03-121"><dt>**PST \_AC \_ 最 \_ 上層 \_ 呼叫者**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dfd03-121"><dt>**PST\_AC\_TOP\_LEVEL\_CALLER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="dfd03-122">最上層呼叫端必須通過檢查，但可能有中繼 Dll。</span><span class="sxs-lookup"><span data-stu-id="dfd03-122">The top-level caller must pass the check, but there may be intermediate DLLs.</span></span> <span data-ttu-id="dfd03-123">指定的映射不一定是立即呼叫端，而是應用程式 ( .exe) 。</span><span class="sxs-lookup"><span data-stu-id="dfd03-123">The specified image is not necessarily the immediate caller, and is an application (.exe).</span></span><br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <span data-ttu-id="dfd03-124"><dt>**PST \_AC \_ 立即 \_ 呼叫者**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dfd03-124"><dt>**PST\_AC\_IMMEDIATE\_CALLER**</dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="dfd03-125">立即呼叫端必須通過檢查，但不需要是最上層的進程。</span><span class="sxs-lookup"><span data-stu-id="dfd03-125">The immediate caller must pass the check, but need not be the top-level process.</span></span> <span data-ttu-id="dfd03-126">指定的影像是立即呼叫端，而影像可以是應用程式 ( .exe) 或 DLL。</span><span class="sxs-lookup"><span data-stu-id="dfd03-126">The specified image is the immediate caller, and the image can be an application (.exe) or a DLL.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dfd03-127">**szRootCA**</span><span class="sxs-lookup"><span data-stu-id="dfd03-127">**szRootCA**</span></span>
</dt> <dd>

<span data-ttu-id="dfd03-128">寬字元字串的指標，代表憑證 (CA) 的根憑證授權單位。使用 **Null** 來使用任何可用的 CA。</span><span class="sxs-lookup"><span data-stu-id="dfd03-128">A pointer to a wide character string that represents the root certification authority (CA) for the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="dfd03-129">**szIssuer**</span><span class="sxs-lookup"><span data-stu-id="dfd03-129">**szIssuer**</span></span>
</dt> <dd>

<span data-ttu-id="dfd03-130">代表發出憑證之 CA 的寬字元字串指標。使用 **Null** 來使用任何可用的 CA。</span><span class="sxs-lookup"><span data-stu-id="dfd03-130">A pointer to a wide character string that represents the CA that issued the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="dfd03-131">**szPublisher**</span><span class="sxs-lookup"><span data-stu-id="dfd03-131">**szPublisher**</span></span>
</dt> <dd>

<span data-ttu-id="dfd03-132">代表軟體發行者的寬字元字串指標。使用 **Null** 來使用任何可用的 CA。</span><span class="sxs-lookup"><span data-stu-id="dfd03-132">A pointer to a wide character string that represents the software publisher; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="dfd03-133">**szProgramName**</span><span class="sxs-lookup"><span data-stu-id="dfd03-133">**szProgramName**</span></span>
</dt> <dd>

<span data-ttu-id="dfd03-134">代表程式名稱的寬字元字串指標。使用 **Null** 來使用任何可用的 CA。</span><span class="sxs-lookup"><span data-stu-id="dfd03-134">A pointer to a wide character string that represents the program name; use **NULL** to use any available CA.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfd03-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfd03-135">Requirements</span></span>



| <span data-ttu-id="dfd03-136">需求</span><span class="sxs-lookup"><span data-stu-id="dfd03-136">Requirement</span></span> | <span data-ttu-id="dfd03-137">值</span><span class="sxs-lookup"><span data-stu-id="dfd03-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd03-138">標頭</span><span class="sxs-lookup"><span data-stu-id="dfd03-138">Header</span></span><br/> | <dl> <span data-ttu-id="dfd03-139"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="dfd03-139"><dt>Pstore.h</dt></span></span> </dl> |



 

 
