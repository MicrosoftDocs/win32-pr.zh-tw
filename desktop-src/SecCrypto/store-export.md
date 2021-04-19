---
description: 將開啟的憑證存放區的內容複寫到已編碼的字串。
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Store. Export 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990753"
---
# <a name="storeexport-method"></a><span data-ttu-id="a24a5-103">Store. Export 方法</span><span class="sxs-lookup"><span data-stu-id="a24a5-103">Store.Export method</span></span>

<span data-ttu-id="a24a5-104">\[**匯出** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a24a5-104">\[The **Export** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a24a5-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="a24a5-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a24a5-106">**Export** 方法會將開啟的 [*憑證存放區*](../secgloss/c-gly.md)的內容複寫到已編碼的字串。</span><span class="sxs-lookup"><span data-stu-id="a24a5-106">The **Export** method copies the contents of an open [*certificate store*](../secgloss/c-gly.md) to an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a24a5-107">語法</span><span class="sxs-lookup"><span data-stu-id="a24a5-107">Syntax</span></span>


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a24a5-108">參數</span><span class="sxs-lookup"><span data-stu-id="a24a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a24a5-109">*SaveAs* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a24a5-109">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a24a5-110">指定匯出作業格式之 [CAPICOM \_ 存放區的儲存 \_ \_ 為 \_ 類型](capicom-store-save-as-type.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="a24a5-110">A value of the [CAPICOM\_STORE\_SAVE\_AS\_TYPE](capicom-store-save-as-type.md) enumeration that indicates the format for the export operation.</span></span> <span data-ttu-id="a24a5-111">預設值為 [ \_ 儲存為序列化的 CAPICOM 存放區] \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="a24a5-111">The default value is CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED.</span></span> <span data-ttu-id="a24a5-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a24a5-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a24a5-113">值</span><span class="sxs-lookup"><span data-stu-id="a24a5-113">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="a24a5-114">意義</span><span class="sxs-lookup"><span data-stu-id="a24a5-114">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <span data-ttu-id="a24a5-115"><dt>**\_將 CAPICOM 儲存區儲存 \_ 為已 \_ \_ 序列化**</dt></span><span class="sxs-lookup"><span data-stu-id="a24a5-115"><dt>**CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="a24a5-116">存放區是以序列化格式儲存。</span><span class="sxs-lookup"><span data-stu-id="a24a5-116">The store is saved in serialized format.</span></span><br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <span data-ttu-id="a24a5-117"><dt>**\_將 CAPICOM 存放區 \_ 另存 \_ 為 \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="a24a5-117"><dt>**CAPICOM\_STORE\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="a24a5-118">存放區是以 PKCS \# 7 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="a24a5-118">The store is saved in PKCS \#7 format.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a24a5-119">*Edi.encodingtype* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a24a5-119">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a24a5-120">[CAPICOM \_ 編碼 \_ 類型](capicom-encoding-type.md)列舉的值，表示匯出之存放區的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="a24a5-120">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates the encoding type of the exported store.</span></span> <span data-ttu-id="a24a5-121">預設值為 CAPICOM \_ 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="a24a5-121">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="a24a5-122">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a24a5-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a24a5-123">值</span><span class="sxs-lookup"><span data-stu-id="a24a5-123">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="a24a5-124">意義</span><span class="sxs-lookup"><span data-stu-id="a24a5-124">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="a24a5-125"><dt>**CAPICOM \_ 編碼 \_ 任何**</dt></span><span class="sxs-lookup"><span data-stu-id="a24a5-125"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="a24a5-126">只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。</span><span class="sxs-lookup"><span data-stu-id="a24a5-126">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="a24a5-127">如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。</span><span class="sxs-lookup"><span data-stu-id="a24a5-127">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="a24a5-128">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="a24a5-128">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="a24a5-129"><dt>**CAPICOM \_ 編碼 \_ BASE64**</dt></span><span class="sxs-lookup"><span data-stu-id="a24a5-129"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="a24a5-130">資料會儲存為 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="a24a5-130">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="a24a5-131"><dt>**CAPICOM \_ 編碼 \_ 二進位**</dt></span><span class="sxs-lookup"><span data-stu-id="a24a5-131"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="a24a5-132">資料會儲存為純二進位序列。</span><span class="sxs-lookup"><span data-stu-id="a24a5-132">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a24a5-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="a24a5-133">Return value</span></span>

<span data-ttu-id="a24a5-134">這個方法會傳回字串，其中包含指定編碼形式之存放區中的憑證。</span><span class="sxs-lookup"><span data-stu-id="a24a5-134">This method returns a string that contains the certificates in the store in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24a5-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="a24a5-135">Requirements</span></span>



| <span data-ttu-id="a24a5-136">需求</span><span class="sxs-lookup"><span data-stu-id="a24a5-136">Requirement</span></span> | <span data-ttu-id="a24a5-137">值</span><span class="sxs-lookup"><span data-stu-id="a24a5-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a24a5-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a24a5-138">Redistributable</span></span><br/> | <span data-ttu-id="a24a5-139">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a24a5-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a24a5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a24a5-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="a24a5-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a24a5-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24a5-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a24a5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24a5-143">**市集**</span><span class="sxs-lookup"><span data-stu-id="a24a5-143">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="a24a5-144">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="a24a5-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
