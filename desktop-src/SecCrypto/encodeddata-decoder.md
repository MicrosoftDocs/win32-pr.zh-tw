---
description: 取得解碼器物件（如果有的話）。
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: EncodedData 解碼方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990760"
---
# <a name="encodeddatadecoder-method"></a><span data-ttu-id="44f1d-103">EncodedData 解碼方法</span><span class="sxs-lookup"><span data-stu-id="44f1d-103">EncodedData.Decoder method</span></span>

<span data-ttu-id="44f1d-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="44f1d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="44f1d-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**AsnEncodedData 類別**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="44f1d-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="44f1d-106">如果有一個解碼器物件存在， **則此方法** 會取得該物件。</span><span class="sxs-lookup"><span data-stu-id="44f1d-106">The **Decoder** method obtains a decoder object, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f1d-107">語法</span><span class="sxs-lookup"><span data-stu-id="44f1d-107">Syntax</span></span>


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a><span data-ttu-id="44f1d-108">參數</span><span class="sxs-lookup"><span data-stu-id="44f1d-108">Parameters</span></span>

<span data-ttu-id="44f1d-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="44f1d-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f1d-110">備註</span><span class="sxs-lookup"><span data-stu-id="44f1d-110">Remarks</span></span>

<span data-ttu-id="44f1d-111">如果編碼的資料沒有解碼器物件，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="44f1d-111">If the encoded data does not have a decoder object, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="44f1d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="44f1d-112">Requirements</span></span>



| <span data-ttu-id="44f1d-113">需求</span><span class="sxs-lookup"><span data-stu-id="44f1d-113">Requirement</span></span> | <span data-ttu-id="44f1d-114">值</span><span class="sxs-lookup"><span data-stu-id="44f1d-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44f1d-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="44f1d-115">End of client support</span></span><br/> | <span data-ttu-id="44f1d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44f1d-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="44f1d-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="44f1d-117">End of server support</span></span><br/> | <span data-ttu-id="44f1d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44f1d-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="44f1d-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="44f1d-119">Redistributable</span></span><br/>       | <span data-ttu-id="44f1d-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="44f1d-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="44f1d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="44f1d-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="44f1d-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44f1d-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
