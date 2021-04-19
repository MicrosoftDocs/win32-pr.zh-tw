---
description: 包含 D3DAUTHENTICATEDCONFIGURE CRYPTOSESSION 命令的輸入資料 \_ 。
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2b1cca13bcd37e488cd0ed455098afa62492579f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973196"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a><span data-ttu-id="b9bd8-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION 結構</span><span class="sxs-lookup"><span data-stu-id="b9bd8-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION structure</span></span>

<span data-ttu-id="b9bd8-104">包含 [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) 命令的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="b9bd8-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) command.</span></span>

<span data-ttu-id="b9bd8-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)。</span><span class="sxs-lookup"><span data-stu-id="b9bd8-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9bd8-106">語法</span><span class="sxs-lookup"><span data-stu-id="b9bd8-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a><span data-ttu-id="b9bd8-107">成員</span><span class="sxs-lookup"><span data-stu-id="b9bd8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9bd8-108">**參數**</span><span class="sxs-lookup"><span data-stu-id="b9bd8-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="b9bd8-109">D3DAUTHENTICATEDCHANNEL 設定包含命令 GUID 和其他資料的 [**\_ \_ 輸入**](d3dauthenticatedchannel-configure-input.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="b9bd8-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="b9bd8-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="b9bd8-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b9bd8-111">DirectX Video 加速 2 (DXVA-2) 解碼器裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b9bd8-111">A handle to the DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="b9bd8-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="b9bd8-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b9bd8-113">密碼編譯會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b9bd8-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="b9bd8-114">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="b9bd8-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b9bd8-115">Direct3D 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b9bd8-115">A handle to the Direct3D device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9bd8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9bd8-116">Requirements</span></span>



| <span data-ttu-id="b9bd8-117">需求</span><span class="sxs-lookup"><span data-stu-id="b9bd8-117">Requirement</span></span> | <span data-ttu-id="b9bd8-118">值</span><span class="sxs-lookup"><span data-stu-id="b9bd8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9bd8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9bd8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b9bd8-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9bd8-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b9bd8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9bd8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b9bd8-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9bd8-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b9bd8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b9bd8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9bd8-124"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9bd8-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9bd8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9bd8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9bd8-126">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="b9bd8-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="b9bd8-127">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="b9bd8-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




