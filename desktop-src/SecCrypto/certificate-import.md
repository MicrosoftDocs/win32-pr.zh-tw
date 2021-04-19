---
description: 從字串將先前編碼的憑證匯入到憑證物件中。
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: ICertificate2：： Import 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea639f1cd89b673ecf8da77302e3d812894a202b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987045"
---
# <a name="icertificate2import-method"></a><span data-ttu-id="3f209-103">ICertificate2：： Import 方法</span><span class="sxs-lookup"><span data-stu-id="3f209-103">ICertificate2::Import method</span></span>

<span data-ttu-id="3f209-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="3f209-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3f209-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="3f209-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3f209-106">匯 **入** 方法會將先前編碼的憑證從字串匯入到 [**憑證**](certificate.md) 物件中。</span><span class="sxs-lookup"><span data-stu-id="3f209-106">The **Import** method imports a previously encoded certificate from a string into the [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="3f209-107">呼叫這個方法會重設這個物件的 [*狀態*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="3f209-107">Calling this method resets the [*state*](../secgloss/s-gly.md) of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f209-108">語法</span><span class="sxs-lookup"><span data-stu-id="3f209-108">Syntax</span></span>


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a><span data-ttu-id="3f209-109">參數</span><span class="sxs-lookup"><span data-stu-id="3f209-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f209-110">*EncodedCertificate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f209-110">*EncodedCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f209-111">字串，包含要匯入的編碼憑證資料。</span><span class="sxs-lookup"><span data-stu-id="3f209-111">A string that contains the encoded certificate data to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f209-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f209-112">Return value</span></span>

<span data-ttu-id="3f209-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3f209-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f209-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f209-114">Requirements</span></span>



| <span data-ttu-id="3f209-115">需求</span><span class="sxs-lookup"><span data-stu-id="3f209-115">Requirement</span></span> | <span data-ttu-id="3f209-116">值</span><span class="sxs-lookup"><span data-stu-id="3f209-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f209-117">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3f209-117">End of client support</span></span><br/> | <span data-ttu-id="3f209-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f209-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3f209-119">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="3f209-119">End of server support</span></span><br/> | <span data-ttu-id="3f209-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f209-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3f209-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="3f209-121">Redistributable</span></span><br/>       | <span data-ttu-id="3f209-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3f209-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3f209-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3f209-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3f209-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f209-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f209-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f209-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f209-126">加密物件</span><span class="sxs-lookup"><span data-stu-id="3f209-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="3f209-127">**憑證**</span><span class="sxs-lookup"><span data-stu-id="3f209-127">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
