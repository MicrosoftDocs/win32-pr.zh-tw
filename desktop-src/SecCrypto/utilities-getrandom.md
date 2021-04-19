---
description: 使用預設密碼編譯服務提供者 (CSP) 來產生安全的亂數。
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: GetRandom 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995292"
---
# <a name="utilitiesgetrandom-method"></a><span data-ttu-id="8a075-103">GetRandom 方法</span><span class="sxs-lookup"><span data-stu-id="8a075-103">Utilities.GetRandom method</span></span>

<span data-ttu-id="8a075-104">\[**GetRandom** 方法可用於 [需求] 區段中指定的作業系統。\]</span><span class="sxs-lookup"><span data-stu-id="8a075-104">\[The **GetRandom** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="8a075-105">**GetRandom** 方法會使用預設 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 來產生安全的亂數。</span><span class="sxs-lookup"><span data-stu-id="8a075-105">The **GetRandom** method generates a secure random number using the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a075-106">語法</span><span class="sxs-lookup"><span data-stu-id="8a075-106">Syntax</span></span>


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8a075-107">參數</span><span class="sxs-lookup"><span data-stu-id="8a075-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a075-108">*長度* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8a075-108">*Length* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a075-109">要建立之亂數字的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8a075-109">The length, in bytes, of the random number to create.</span></span> <span data-ttu-id="8a075-110">預設值為8個位元組。</span><span class="sxs-lookup"><span data-stu-id="8a075-110">The default value is 8 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8a075-111">*Edi.encodingtype* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8a075-111">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a075-112">[**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)列舉的值，表示要用於產生之亂數字的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="8a075-112">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the type of encoding to use for the generated random number.</span></span> <span data-ttu-id="8a075-113">預設值為 [CAPICOM \_ 編碼 \_ 二進位]。</span><span class="sxs-lookup"><span data-stu-id="8a075-113">The default value is CAPICOM\_ENCODE\_BINARY.</span></span> <span data-ttu-id="8a075-114">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8a075-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8a075-115">值</span><span class="sxs-lookup"><span data-stu-id="8a075-115">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="8a075-116">意義</span><span class="sxs-lookup"><span data-stu-id="8a075-116">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="8a075-117"><dt>**CAPICOM \_ 編碼 \_ 任何**</dt></span><span class="sxs-lookup"><span data-stu-id="8a075-117"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="8a075-118">只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。</span><span class="sxs-lookup"><span data-stu-id="8a075-118">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="8a075-119">如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="8a075-119">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="8a075-120">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="8a075-120">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="8a075-121"><dt>**CAPICOM \_ 編碼 \_ BASE64**</dt></span><span class="sxs-lookup"><span data-stu-id="8a075-121"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="8a075-122">資料會儲存為 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="8a075-122">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="8a075-123"><dt>**CAPICOM \_ 編碼 \_ 二進位**</dt></span><span class="sxs-lookup"><span data-stu-id="8a075-123"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="8a075-124">資料會儲存為純二進位序列。</span><span class="sxs-lookup"><span data-stu-id="8a075-124">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a075-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a075-125">Return value</span></span>

<span data-ttu-id="8a075-126">隨機產生的數位 *長度* 位元組長，具有指定的編碼。</span><span class="sxs-lookup"><span data-stu-id="8a075-126">A randomly generated number *Length* bytes long, with the specified encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a075-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a075-127">Requirements</span></span>



| <span data-ttu-id="8a075-128">需求</span><span class="sxs-lookup"><span data-stu-id="8a075-128">Requirement</span></span> | <span data-ttu-id="8a075-129">值</span><span class="sxs-lookup"><span data-stu-id="8a075-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a075-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8a075-130">Redistributable</span></span><br/> | <span data-ttu-id="8a075-131">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8a075-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8a075-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8a075-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="8a075-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a075-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a075-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a075-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a075-135">**公用程式**</span><span class="sxs-lookup"><span data-stu-id="8a075-135">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 
