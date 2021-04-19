---
description: 將憑證複製到編碼的字串。
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: ICertificate2：： Export 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995050"
---
# <a name="icertificate2export-method"></a><span data-ttu-id="33fb9-103">ICertificate2：： Export 方法</span><span class="sxs-lookup"><span data-stu-id="33fb9-103">ICertificate2::Export method</span></span>

<span data-ttu-id="33fb9-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="33fb9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="33fb9-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="33fb9-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="33fb9-106">**Export** 方法會將憑證複製到編碼的字串。</span><span class="sxs-lookup"><span data-stu-id="33fb9-106">The **Export** method copies a certificate to an encoded string.</span></span> <span data-ttu-id="33fb9-107">編碼的字串可以寫入檔案或匯入至新的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="33fb9-107">The encoded string can be written to a file or imported into a new [**Certificate**](certificate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="33fb9-108">語法</span><span class="sxs-lookup"><span data-stu-id="33fb9-108">Syntax</span></span>


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="33fb9-109">參數</span><span class="sxs-lookup"><span data-stu-id="33fb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33fb9-110">*Edi.encodingtype* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="33fb9-110">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33fb9-111">[**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)列舉值，指定匯出作業的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="33fb9-111">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that specifies the encoding type for the export operation.</span></span> <span data-ttu-id="33fb9-112">預設值為 **CAPICOM \_ 編碼 \_ BASE64**。</span><span class="sxs-lookup"><span data-stu-id="33fb9-112">The default value is **CAPICOM\_ENCODE\_BASE64**.</span></span> <span data-ttu-id="33fb9-113">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="33fb9-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="33fb9-114">值</span><span class="sxs-lookup"><span data-stu-id="33fb9-114">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="33fb9-115">意義</span><span class="sxs-lookup"><span data-stu-id="33fb9-115">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="33fb9-116"><dt>**CAPICOM \_ 編碼 \_ 任何**</dt></span><span class="sxs-lookup"><span data-stu-id="33fb9-116"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="33fb9-117">只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。</span><span class="sxs-lookup"><span data-stu-id="33fb9-117">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="33fb9-118">如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="33fb9-118">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="33fb9-119">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="33fb9-119">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="33fb9-120"><dt>**CAPICOM \_ 編碼 \_ BASE64**</dt></span><span class="sxs-lookup"><span data-stu-id="33fb9-120"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="33fb9-121">資料會儲存為 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="33fb9-121">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="33fb9-122"><dt>**CAPICOM \_ 編碼 \_ 二進位**</dt></span><span class="sxs-lookup"><span data-stu-id="33fb9-122"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="33fb9-123">資料會儲存為純二進位序列。</span><span class="sxs-lookup"><span data-stu-id="33fb9-123">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33fb9-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="33fb9-124">Return value</span></span>

<span data-ttu-id="33fb9-125">字串，其中包含以指定編碼形式匯出的憑證。</span><span class="sxs-lookup"><span data-stu-id="33fb9-125">A string that contains the exported certificate in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="33fb9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="33fb9-126">Requirements</span></span>



| <span data-ttu-id="33fb9-127">需求</span><span class="sxs-lookup"><span data-stu-id="33fb9-127">Requirement</span></span> | <span data-ttu-id="33fb9-128">值</span><span class="sxs-lookup"><span data-stu-id="33fb9-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33fb9-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="33fb9-129">End of client support</span></span><br/> | <span data-ttu-id="33fb9-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33fb9-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="33fb9-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="33fb9-131">End of server support</span></span><br/> | <span data-ttu-id="33fb9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33fb9-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="33fb9-133">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="33fb9-133">Redistributable</span></span><br/>       | <span data-ttu-id="33fb9-134">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="33fb9-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="33fb9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="33fb9-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="33fb9-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33fb9-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33fb9-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33fb9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33fb9-138">加密物件</span><span class="sxs-lookup"><span data-stu-id="33fb9-138">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="33fb9-139">**憑證**</span><span class="sxs-lookup"><span data-stu-id="33fb9-139">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
