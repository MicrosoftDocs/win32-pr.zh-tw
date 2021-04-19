---
description: 傳回編碼資料的字串表示。
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: EncodedData 格式方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994831"
---
# <a name="encodeddataformat-method"></a><span data-ttu-id="19216-103">EncodedData 格式方法</span><span class="sxs-lookup"><span data-stu-id="19216-103">EncodedData.Format method</span></span>

<span data-ttu-id="19216-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="19216-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="19216-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**AsnEncodedData 類別**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="19216-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="19216-106">**Format** 方法會傳回已編碼資料的字串表示。</span><span class="sxs-lookup"><span data-stu-id="19216-106">The **Format** method returns a string representation of the encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="19216-107">語法</span><span class="sxs-lookup"><span data-stu-id="19216-107">Syntax</span></span>


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a><span data-ttu-id="19216-108">參數</span><span class="sxs-lookup"><span data-stu-id="19216-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19216-109">*bMultiLines* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="19216-109">*bMultiLines* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19216-110">布林值，指出傳回的字串是否包含多行。</span><span class="sxs-lookup"><span data-stu-id="19216-110">Boolean value that indicates whether the returned string contains multiple lines.</span></span> <span data-ttu-id="19216-111">若 **為 True**，則傳回的字串可能包含多個以 **vbCrLf** 分隔的行。</span><span class="sxs-lookup"><span data-stu-id="19216-111">If **True**, the returned string may contain multiple lines separated by **vbCrLf**.</span></span> <span data-ttu-id="19216-112">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="19216-112">The default value is **False**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19216-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="19216-113">Return value</span></span>

<span data-ttu-id="19216-114">人們可讀取的字串，表示已編碼的資料。</span><span class="sxs-lookup"><span data-stu-id="19216-114">A human-readable string that represents the encoded data.</span></span> <span data-ttu-id="19216-115">如果 CAPICOM 無法理解編碼的資料，就會傳回資料的十六進位標記法。</span><span class="sxs-lookup"><span data-stu-id="19216-115">If CAPICOM does not understand the encoded data, a hexadecimal representation of the data is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="19216-116">備註</span><span class="sxs-lookup"><span data-stu-id="19216-116">Remarks</span></span>

<span data-ttu-id="19216-117">傳回字串的格式可能會在不同版本的 CAPICOM 之間變更。</span><span class="sxs-lookup"><span data-stu-id="19216-117">The format of the returned string may change between different versions of CAPICOM.</span></span> <span data-ttu-id="19216-118">請勿依賴您應用程式中的任何特定格式。</span><span class="sxs-lookup"><span data-stu-id="19216-118">Do not rely on any particular format in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="19216-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="19216-119">Requirements</span></span>



| <span data-ttu-id="19216-120">需求</span><span class="sxs-lookup"><span data-stu-id="19216-120">Requirement</span></span> | <span data-ttu-id="19216-121">值</span><span class="sxs-lookup"><span data-stu-id="19216-121">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19216-122">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="19216-122">End of client support</span></span><br/> | <span data-ttu-id="19216-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19216-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="19216-124">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="19216-124">End of server support</span></span><br/> | <span data-ttu-id="19216-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19216-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="19216-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="19216-126">Redistributable</span></span><br/>       | <span data-ttu-id="19216-127">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="19216-127">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19216-128">DLL</span><span class="sxs-lookup"><span data-stu-id="19216-128">DLL</span></span><br/>                   | <dl> <span data-ttu-id="19216-129"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19216-129"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19216-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19216-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19216-131">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="19216-131">**EncodedData**</span></span>](encodeddata.md)
</dt> </dl>

 

 
