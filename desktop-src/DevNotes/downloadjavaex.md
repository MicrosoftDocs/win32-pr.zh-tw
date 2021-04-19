---
description: 下載 .cab 檔簽章、驗證與封裝相關聯的許可權，並根據驗證執行。
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: DownloadJAVAEX 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999359"
---
# <a name="downloadjavaex-function"></a><span data-ttu-id="4ba82-103">DownloadJAVAEX 函式</span><span class="sxs-lookup"><span data-stu-id="4ba82-103">DownloadJavaEX function</span></span>

<span data-ttu-id="4ba82-104">下載 .cab 檔簽章、驗證與封裝相關聯的許可權，並根據驗證執行。</span><span class="sxs-lookup"><span data-stu-id="4ba82-104">Downloads the .cab file signature, verifies the permissions associated with the packages, and executes them based on authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba82-105">語法</span><span class="sxs-lookup"><span data-stu-id="4ba82-105">Syntax</span></span>


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a><span data-ttu-id="4ba82-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ba82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ba82-107">*保留* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ba82-107">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ba82-108">此參數已保留備用。</span><span class="sxs-lookup"><span data-stu-id="4ba82-108">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4ba82-109">*pProviderData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ba82-109">*pProviderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ba82-110">包含憑證資料的 [**CRYPT \_ 提供者 \_ 資料**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) 結構，例如檔案和區域許可權。</span><span class="sxs-lookup"><span data-stu-id="4ba82-110">A [**CRYPT\_PROVIDER\_DATA**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) structure that contains certificate data such as file and zone permissions.</span></span>

</dd> <dt>

<span data-ttu-id="4ba82-111">*pJAVA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ba82-111">*pJava* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ba82-112">[**JAVA \_ 原則 \_ 提供者**](/previous-versions//bb432350(v=vs.85))結構，其中包含與原則提供者相關的資料。</span><span class="sxs-lookup"><span data-stu-id="4ba82-112">A [**JAVA\_POLICY\_PROVIDER**](/previous-versions//bb432350(v=vs.85)) structure that contains data related to the policy provider.</span></span>

</dd> <dt>

<span data-ttu-id="4ba82-113">*pFunctions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ba82-113">*pFunctions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ba82-114">[**CRYPT \_ 提供者 \_**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions)函式結構，其中包含驗證憑證物件、簽章和最終原則的方法清單。</span><span class="sxs-lookup"><span data-stu-id="4ba82-114">A [**CRYPT\_PROVIDER\_FUNCTIONS**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) structure that contains a list of methods to verify certificate objects, signatures, and final policies.</span></span>

</dd> <dt>

<span data-ttu-id="4ba82-115">*fCertificate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ba82-115">*fCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ba82-116">如果有憑證存在，此參數為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="4ba82-116">If a certificate is present, this parameter is **TRUE**.</span></span> <span data-ttu-id="4ba82-117">否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="4ba82-117">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ba82-118">*pTrust* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ba82-118">*pTrust* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ba82-119">[**JAVA \_ 信任**](/windows/desktop/api/Capi/ns-capi-java_trust)結構，包含信任資訊，例如編碼的許可權、編碼器簽章和真實的傳回原則代碼。</span><span class="sxs-lookup"><span data-stu-id="4ba82-119">A [**JAVA\_TRUST**](/windows/desktop/api/Capi/ns-capi-java_trust) structure that contains trust information such as encoded permission, encoder signature, and authentic return policy code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ba82-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ba82-120">Return value</span></span>

<span data-ttu-id="4ba82-121">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4ba82-121">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="4ba82-122">否則，傳回值會是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4ba82-122">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ba82-123">備註</span><span class="sxs-lookup"><span data-stu-id="4ba82-123">Remarks</span></span>

<span data-ttu-id="4ba82-124">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="4ba82-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ba82-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ba82-125">Requirements</span></span>



| <span data-ttu-id="4ba82-126">需求</span><span class="sxs-lookup"><span data-stu-id="4ba82-126">Requirement</span></span> | <span data-ttu-id="4ba82-127">值</span><span class="sxs-lookup"><span data-stu-id="4ba82-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba82-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4ba82-128">DLL</span></span><br/> | <dl> <span data-ttu-id="4ba82-129"><dt>Javacypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ba82-129"><dt>Javacypt.dll</dt></span></span> </dl> |



 

 
