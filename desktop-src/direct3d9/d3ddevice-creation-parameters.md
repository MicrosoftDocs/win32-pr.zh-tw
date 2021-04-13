---
description: 描述裝置的建立參數。
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: 'D3DDEVICE_CREATION_PARAMETERS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322767"
---
# <a name="d3ddevice_creation_parameters-structure"></a><span data-ttu-id="82a9e-103">D3DDEVICE \_ 建立 \_ 參數結構</span><span class="sxs-lookup"><span data-stu-id="82a9e-103">D3DDEVICE\_CREATION\_PARAMETERS structure</span></span>

<span data-ttu-id="82a9e-104">描述裝置的建立參數。</span><span class="sxs-lookup"><span data-stu-id="82a9e-104">Describes the creation parameters for a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="82a9e-105">Syntax</span></span>


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="82a9e-106">成員</span><span class="sxs-lookup"><span data-stu-id="82a9e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="82a9e-107">**AdapterOrdinal**</span><span class="sxs-lookup"><span data-stu-id="82a9e-107">**AdapterOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="82a9e-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82a9e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82a9e-109">表示顯示配接器的序數。</span><span class="sxs-lookup"><span data-stu-id="82a9e-109">Ordinal number that denotes the display adapter.</span></span> <span data-ttu-id="82a9e-110">D3DADAPTER \_ 預設一律是主顯示器介面卡。</span><span class="sxs-lookup"><span data-stu-id="82a9e-110">D3DADAPTER\_DEFAULT is always the primary display adapter.</span></span> <span data-ttu-id="82a9e-111">使用此序數做為任何 [**IDirect3D9**](/windows/desktop/api) 方法的介面卡參數。</span><span class="sxs-lookup"><span data-stu-id="82a9e-111">Use this ordinal as the Adapter parameter for any of the [**IDirect3D9**](/windows/desktop/api) methods.</span></span> <span data-ttu-id="82a9e-112">請注意，Direct3D 9.0 物件的不同實例可以使用不同的序數。</span><span class="sxs-lookup"><span data-stu-id="82a9e-112">Note that different instances of Direct3D 9.0 objects can use different ordinals.</span></span> <span data-ttu-id="82a9e-113">例如，當使用者新增或移除多個監視器系統中的監視時，或當他們熱交換膝上型電腦時，介面卡可進入或離開系統。</span><span class="sxs-lookup"><span data-stu-id="82a9e-113">Adapters can enter or leave a system when users, for example, add or remove monitors from a multiple-monitor system or when they hot-swap a laptop.</span></span> <span data-ttu-id="82a9e-114">因此，您只能在已知有效的 Direct3D 9.0 實例中使用此序數，也就是建立此 [**IDirect3DDevice9**](/windows/desktop/api) 介面的 direct3d 9.0 或從 [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d)傳回的 direct3d 9.0，如同透過這個 **IDirect3DDevice9** 介面所呼叫。</span><span class="sxs-lookup"><span data-stu-id="82a9e-114">Consequently, use this ordinal only in a Direct3D 9.0 instance known to be valid, that is, either the Direct3D 9.0 that created this [**IDirect3DDevice9**](/windows/desktop/api) interface or the Direct3D 9.0 returned from [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), as called through this **IDirect3DDevice9** interface.</span></span>

</dd> <dt>

<span data-ttu-id="82a9e-115">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="82a9e-115">**DeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="82a9e-116">類型： **[ **D3DDEVTYPE**](./d3ddevtype.md)**</span><span class="sxs-lookup"><span data-stu-id="82a9e-116">Type: **[**D3DDEVTYPE**](./d3ddevtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82a9e-117">[**D3DDEVTYPE**](./d3ddevtype.md)列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="82a9e-117">Member of the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type.</span></span> <span data-ttu-id="82a9e-118">代表此裝置的模擬功能數量。</span><span class="sxs-lookup"><span data-stu-id="82a9e-118">Denotes the amount of emulated functionality for this device.</span></span> <span data-ttu-id="82a9e-119">此參數的值會反映傳遞給建立此裝置之 [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 呼叫的值。</span><span class="sxs-lookup"><span data-stu-id="82a9e-119">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="82a9e-120">**hFocusWindow**</span><span class="sxs-lookup"><span data-stu-id="82a9e-120">**hFocusWindow**</span></span>
</dt> <dd>

<span data-ttu-id="82a9e-121">類型： **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82a9e-121">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82a9e-122">焦點屬於此 Direct3D 裝置的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="82a9e-122">Window handle to which focus belongs for this Direct3D device.</span></span> <span data-ttu-id="82a9e-123">此參數的值會反映傳遞給建立此裝置之 [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 呼叫的值。</span><span class="sxs-lookup"><span data-stu-id="82a9e-123">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="82a9e-124">**BehaviorFlags**</span><span class="sxs-lookup"><span data-stu-id="82a9e-124">**BehaviorFlags**</span></span>
</dt> <dd>

<span data-ttu-id="82a9e-125">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82a9e-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82a9e-126">一或多個 [D3DCREATE](d3dcreate.md) 常數的組合，可控制裝置的全域行為。</span><span class="sxs-lookup"><span data-stu-id="82a9e-126">A combination of one or more [D3DCREATE](d3dcreate.md) constants that control global behavior of the device.</span></span> <span data-ttu-id="82a9e-127">這些常數會在建立裝置時反映傳遞給 [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 的常數。</span><span class="sxs-lookup"><span data-stu-id="82a9e-127">These constants mirror the constants passed to [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) when the device was created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82a9e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="82a9e-128">Requirements</span></span>



| <span data-ttu-id="82a9e-129">需求</span><span class="sxs-lookup"><span data-stu-id="82a9e-129">Requirement</span></span> | <span data-ttu-id="82a9e-130">值</span><span class="sxs-lookup"><span data-stu-id="82a9e-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82a9e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="82a9e-131">Header</span></span><br/> | <dl> <span data-ttu-id="82a9e-132"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="82a9e-132"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82a9e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82a9e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a9e-134">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="82a9e-134">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="82a9e-135">**GetCreationParameters**</span><span class="sxs-lookup"><span data-stu-id="82a9e-135">**GetCreationParameters**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[<span data-ttu-id="82a9e-136">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="82a9e-136">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
