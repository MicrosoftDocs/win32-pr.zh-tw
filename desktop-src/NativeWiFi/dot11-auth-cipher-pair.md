---
description: 定義可同時在802.11 站上啟用的一組802.11 驗證和加密演算法。
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: 'DOT11_AUTH_CIPHER_PAIR 結構 (Wlantypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975753"
---
# <a name="dot11_auth_cipher_pair-structure"></a><span data-ttu-id="2fd24-103">DOT11 \_ AUTH \_ CIPHER \_ 成對結構</span><span class="sxs-lookup"><span data-stu-id="2fd24-103">DOT11\_AUTH\_CIPHER\_PAIR structure</span></span>

<span data-ttu-id="2fd24-104">**DOT11 \_ AUTH \_ CIPHER \_** 組結構會定義一組802.11 驗證和加密演算法，可在802.11 站上同時啟用。</span><span class="sxs-lookup"><span data-stu-id="2fd24-104">The **DOT11\_AUTH\_CIPHER\_PAIR** structure defines a pair of 802.11 authentication and cipher algorithms that can be enabled at the same time on the 802.11 station.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd24-105">語法</span><span class="sxs-lookup"><span data-stu-id="2fd24-105">Syntax</span></span>


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a><span data-ttu-id="2fd24-106">成員</span><span class="sxs-lookup"><span data-stu-id="2fd24-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2fd24-107">**AuthAlgoId**</span><span class="sxs-lookup"><span data-stu-id="2fd24-107">**AuthAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="2fd24-108">使用 [**DOT11 \_ AUTH \_ 演算法**](dot11-auth-algorithm.md) 列舉類型的驗證演算法。</span><span class="sxs-lookup"><span data-stu-id="2fd24-108">An authentication algorithm that uses a [**DOT11\_AUTH\_ALGORITHM**](dot11-auth-algorithm.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="2fd24-109">**CipherAlgoId**</span><span class="sxs-lookup"><span data-stu-id="2fd24-109">**CipherAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="2fd24-110">使用 [**DOT11 \_ cipher \_ 演算法**](dot11-cipher-algorithm.md) 列舉型別的密碼演算法。</span><span class="sxs-lookup"><span data-stu-id="2fd24-110">A cipher algorithm that uses a [**DOT11\_CIPHER\_ALGORITHM**](dot11-cipher-algorithm.md) enumerated type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fd24-111">備註</span><span class="sxs-lookup"><span data-stu-id="2fd24-111">Remarks</span></span>

<span data-ttu-id="2fd24-112">DOT11 \_ AUTH \_ CIPHER 的 \_ 結構定義了一種驗證和密碼演算法，可同時為基本服務集 (BSS) 網路連線啟用。</span><span class="sxs-lookup"><span data-stu-id="2fd24-112">The DOT11\_AUTH\_CIPHER\_PAIR structure defines an authentication and cipher algorithm that can be enabled together for basic service set (BSS) network connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd24-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fd24-113">Requirements</span></span>



| <span data-ttu-id="2fd24-114">需求</span><span class="sxs-lookup"><span data-stu-id="2fd24-114">Requirement</span></span> | <span data-ttu-id="2fd24-115">值</span><span class="sxs-lookup"><span data-stu-id="2fd24-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd24-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fd24-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd24-117">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fd24-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2fd24-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fd24-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd24-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fd24-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="2fd24-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2fd24-120">Redistributable</span></span><br/>          | <span data-ttu-id="2fd24-121">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="2fd24-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="2fd24-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2fd24-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fd24-123"><dt>Wlantypes (包含 Windot11) </dt></span><span class="sxs-lookup"><span data-stu-id="2fd24-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd24-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fd24-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd24-125">**DOT11 \_ AUTH \_ 演算法**</span><span class="sxs-lookup"><span data-stu-id="2fd24-125">**DOT11\_AUTH\_ALGORITHM**</span></span>](dot11-auth-algorithm.md)
</dt> <dt>

[<span data-ttu-id="2fd24-126">**DOT11 \_ 密碼 \_ 演算法**</span><span class="sxs-lookup"><span data-stu-id="2fd24-126">**DOT11\_CIPHER\_ALGORITHM**</span></span>](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




