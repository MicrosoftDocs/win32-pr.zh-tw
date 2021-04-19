---
title: 'WMDRMCryptoData 結構 (Wmdrmsdk .h) '
description: WMDRMCryptoData 結構包含用來加密和解密內容的密碼編譯演算法的相關資訊。
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- WMDRMCryptoData 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999377"
---
# <a name="wmdrmcryptodata-structure"></a><span data-ttu-id="7acf3-105">WMDRMCryptoData 結構</span><span class="sxs-lookup"><span data-stu-id="7acf3-105">WMDRMCryptoData structure</span></span>

<span data-ttu-id="7acf3-106">**WMDRMCryptoData** 結構包含用來加密和解密內容的密碼編譯演算法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7acf3-106">The **WMDRMCryptoData** structure contains information about the cryptographic algorithm used to encrypt and decrypt content.</span></span>

## <a name="syntax"></a><span data-ttu-id="7acf3-107">語法</span><span class="sxs-lookup"><span data-stu-id="7acf3-107">Syntax</span></span>


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a><span data-ttu-id="7acf3-108">成員</span><span class="sxs-lookup"><span data-stu-id="7acf3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7acf3-109">**cryptoType**</span><span class="sxs-lookup"><span data-stu-id="7acf3-109">**cryptoType**</span></span>
</dt> <dd>

<span data-ttu-id="7acf3-110">[**DRM \_ 加密 \_ 類型**](drm-crypto-type.md)列舉的成員，指定密碼編譯演算法的類型。</span><span class="sxs-lookup"><span data-stu-id="7acf3-110">Member of the [**DRM\_CRYPTO\_TYPE**](drm-crypto-type.md) enumeration specifying the type of cryptographic algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="7acf3-111">**qwCounterID**</span><span class="sxs-lookup"><span data-stu-id="7acf3-111">**qwCounterID**</span></span>
</dt> <dd>

<span data-ttu-id="7acf3-112">128位 AES 計數器模式的高64位。</span><span class="sxs-lookup"><span data-stu-id="7acf3-112">The high 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="7acf3-113">只有當 **cryptoType** 成員設定為 **加密 \_ 類型 \_ MCE** 時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="7acf3-113">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> <dt>

<span data-ttu-id="7acf3-114">**qwOffset**</span><span class="sxs-lookup"><span data-stu-id="7acf3-114">**qwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7acf3-115">128位 AES 計數器模式的低64位。</span><span class="sxs-lookup"><span data-stu-id="7acf3-115">The low 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="7acf3-116">只有當 **cryptoType** 成員設定為 **加密 \_ 類型 \_ MCE** 時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="7acf3-116">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7acf3-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7acf3-117">Requirements</span></span>



| <span data-ttu-id="7acf3-118">需求</span><span class="sxs-lookup"><span data-stu-id="7acf3-118">Requirement</span></span> | <span data-ttu-id="7acf3-119">值</span><span class="sxs-lookup"><span data-stu-id="7acf3-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7acf3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7acf3-120">Header</span></span><br/> | <dl> <span data-ttu-id="7acf3-121"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="7acf3-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7acf3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7acf3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7acf3-123">**結構**</span><span class="sxs-lookup"><span data-stu-id="7acf3-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





