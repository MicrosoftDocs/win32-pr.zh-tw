---
description: 指定 (CA) 的憑證授權單位單位名稱。
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: ISCrdEnr：： setCAName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988953"
---
# <a name="iscrdenrsetcaname-method"></a><span data-ttu-id="3ddd9-103">ISCrdEnr：： setCAName 方法</span><span class="sxs-lookup"><span data-stu-id="3ddd9-103">ISCrdEnr::setCAName method</span></span>

<span data-ttu-id="3ddd9-104">**SetCAName** 方法會指定 (CA) 的 [*憑證授權單位*](../secgloss/c-gly.md)單位名稱。</span><span class="sxs-lookup"><span data-stu-id="3ddd9-104">The **setCAName** method specifies the name of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ddd9-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ddd9-105">Syntax</span></span>


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="3ddd9-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ddd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ddd9-107">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ddd9-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddd9-108">值，指定名稱是指 CA 名稱或 CA 的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="3ddd9-108">Value that specifies whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="3ddd9-109">如果此值為捨棄 \_ 註冊 \_ CA \_ 電腦 \_ 名稱 (定義為 0x01) ，則名稱會參考 CA 的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="3ddd9-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="3ddd9-110">否則，名稱會參考 CA 名稱。</span><span class="sxs-lookup"><span data-stu-id="3ddd9-110">Otherwise, the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="3ddd9-111">*bstrCertTemplateName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ddd9-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddd9-112">憑證範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ddd9-112">Name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="3ddd9-113">*bstrCAName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ddd9-113">*bstrCAName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddd9-114">要與 *bstrCertTemplateName* 所指定的憑證範本搭配使用的 CA 名稱。</span><span class="sxs-lookup"><span data-stu-id="3ddd9-114">CA name to be used with the certificate template specified by *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ddd9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ddd9-115">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="3ddd9-116">VB</span><span class="sxs-lookup"><span data-stu-id="3ddd9-116">VB</span></span>

<span data-ttu-id="3ddd9-117">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="3ddd9-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="3ddd9-118">S 的值 \_ 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="3ddd9-118">A value of S\_OK indicates that the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ddd9-119">備註</span><span class="sxs-lookup"><span data-stu-id="3ddd9-119">Remarks</span></span>

<span data-ttu-id="3ddd9-120">使用這個方法來指定憑證範本的 CA。</span><span class="sxs-lookup"><span data-stu-id="3ddd9-120">Use this method to specify a CA for a certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddd9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ddd9-121">Requirements</span></span>



| <span data-ttu-id="3ddd9-122">需求</span><span class="sxs-lookup"><span data-stu-id="3ddd9-122">Requirement</span></span> | <span data-ttu-id="3ddd9-123">值</span><span class="sxs-lookup"><span data-stu-id="3ddd9-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddd9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ddd9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3ddd9-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="3ddd9-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3ddd9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ddd9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3ddd9-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ddd9-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ddd9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3ddd9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ddd9-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ddd9-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ddd9-130">IID</span><span class="sxs-lookup"><span data-stu-id="3ddd9-130">IID</span></span><br/>                      | <span data-ttu-id="3ddd9-131">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="3ddd9-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="3ddd9-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ddd9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddd9-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="3ddd9-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="3ddd9-134">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="3ddd9-134">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="3ddd9-135">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="3ddd9-135">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
