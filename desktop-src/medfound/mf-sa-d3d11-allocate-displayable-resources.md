---
description: 指定 MFT 的範例配置器 (SA) 是否應使用 D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE 旗標配置基礎 Direct3D 材質。
title: 'MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES (Mftransform) '
ms.topic: reference
ms.date: 03/31/2018
ms.openlocfilehash: ac70ee8c3015a2e08df2ee78b8051723707a1686
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2021
ms.locfileid: "107224021"
---
# <a name="mf_sa_d3d_allocate_displayable_resources-attribute"></a><span data-ttu-id="276c0-103">MF \_ SA \_ D3D 配置可顯示的 \_ \_ \_ 資源屬性</span><span class="sxs-lookup"><span data-stu-id="276c0-103">MF\_SA\_D3D\_ALLOCATE\_DISPLAYABLE\_RESOURCES attribute</span></span>

<span data-ttu-id="276c0-104">指定 MFT 的範例配置器 (SA) 是否應使用 [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) 旗標配置基礎 Direct3D 材質。</span><span class="sxs-lookup"><span data-stu-id="276c0-104">Specifies if the MFT’s Sample Allocator (SA) should allocate the underlying Direct3D Texture using the [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> 

## <a name="data-type"></a><span data-ttu-id="276c0-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="276c0-105">Data type</span></span>

<span data-ttu-id="276c0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="276c0-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="276c0-107">備註</span><span class="sxs-lookup"><span data-stu-id="276c0-107">Remarks</span></span>

<span data-ttu-id="276c0-108">此屬性可在 Windows 10 Preview 組建14383中使用開始。</span><span class="sxs-lookup"><span data-stu-id="276c0-108">This attribute is available staring with Windows 10 Preview build 14383.</span></span> 

> [!NOTE]
> <span data-ttu-id="276c0-109">未來的 SDK 版本將提供 [D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)列舉的 **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** 成員欄位。</span><span class="sxs-lookup"><span data-stu-id="276c0-109">The **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** member field of the [D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration will be available in a future release of the SDK.</span></span>

<span data-ttu-id="276c0-110">媒體基礎平台層會在轉譯影片時設定 **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** 屬性。</span><span class="sxs-lookup"><span data-stu-id="276c0-110">The Media Foundation platform layer sets the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute when rendering video.</span></span> <span data-ttu-id="276c0-111">如果應用程式想要執行自己的影片轉譯器，並利用 D3D11 可顯示的資源，則應用程式也可以選擇設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="276c0-111">An app could also opt to set this attribute if it wants to implement its own video renderer and make use of D3D11 Displayable Resources.</span></span> 

## <a name="example"></a><span data-ttu-id="276c0-112">範例</span><span class="sxs-lookup"><span data-stu-id="276c0-112">Example</span></span>

<span data-ttu-id="276c0-113">下列程式碼範例將示範 **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** 屬性的使用方式。</span><span class="sxs-lookup"><span data-stu-id="276c0-113">The following code example demonstrates the usage of the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute.</span></span>

```cpp
class DecoderMFT : public IMFAttributes, public IMFTransform 
{ 
    //  
    ... Other implementation details ommitted 
    // 

public: 
    // Implementation of IMFAttributes::GetAttributes which is invoked by the MF Topology Loader 
    STDMETHODIMP GetAttribtues(IMFAttributes** attributes) 
    { 
        m_attributes.copyTo(attributes); 
        return S_OK; 
    } 

 

private: 
    // Private method to be called before DecoderMFT initializes its sample pool. 
    // A good place for this to happen is in the method which processes the  
    // 'MFT_MESSAGE_NOTIFY_BEGIN_STREAMING' event. 
    // At a minimum, this processing would be in DecoderMFT's implementation of IMFTransform::ProcessMessage.  

    HRESULT ConfigureTextureFlags() 
    { 
        UINT32 allocateDisplayables = MFGetAttributeUINT32(m_attributes.get(), 
            MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES, 0); 

        // If no MF_SA_* attributes which correspond to D3D misc flags are set then it is valid for 
        // miscFlags to be set to 0. 
        m_textureDesc.miscFlags = 0; 
        UINT32 sharedResources = 0; 

        if (allocateDisplayables != 0) 
        { 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_DISPLAYABLE; 
            // The following flag is required for the decoders output to 
            // use D3D11_RESOURCE_MISC_DISPLAYABLE. 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_EXCLUSIVE_WRITER; 

            // The following flags are required for the presentation API 
            // to consume and present these resources (also known as direct presentation). 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED_NTHANDLE; 

            sharedResources = 1; 
        } 
        else  
        { 
            // This handles the case when MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES was 0 or missing. 
            sharedResources = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED_WITHOUT_MUTEX, 0); 

            if (sharedResources != 0) 
            { 
                m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            } 
            else 
            { 
                UINT32 sharedKeyMutex = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED, 0); 

                if (sharedKeyMutex != 0) 
                { 
                    m_textureDesc.micsFlags |= D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX; 
                } 
            } 
        } 

        // Processing for other MF_SA_* attributes which imply D3D11_RESOURCE_MISC flag 
        // omitted from this sample. 

        return S_OK; 

    } 

    // Private method showing how DecoderMFT can create a texture with the flags required 
    // to satisfy "MF_SA_D3D11_ALLOCATE_DISPLAYBLE_RESOURCES".  
    // Because this is a private function we know the passed in pointer is always valid. 
    // This would be invoked by another private DecoderMFT function when allocating an MFSample 
    // for its sample pool. 

    HRESULT AllocateTextureForSample(ID3D11Texture2D** texture2D) 
    { 
        return m_d3dDevice->CreateTexture2D(&m_textureDesc, nullptr, texture2D); 
    } 

    // ... other members omitted 
    wil::com_ptr_nothrow<IMFAttributes> m_attributes; 
    wil::com_ptr_nothrow<ID3D11Device> m_d3dDevice; 

    // This a texture description for D3D11 resources. 
    D3D11_TEXTURE_2D_DESC m_textureDesc = {}; 

}; 
```

## <a name="requirements"></a><span data-ttu-id="276c0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="276c0-114">Requirements</span></span>



| <span data-ttu-id="276c0-115">需求</span><span class="sxs-lookup"><span data-stu-id="276c0-115">Requirement</span></span> | <span data-ttu-id="276c0-116">值</span><span class="sxs-lookup"><span data-stu-id="276c0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="276c0-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="276c0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="276c0-118">Windows 10 Preview 組建14383</span><span class="sxs-lookup"><span data-stu-id="276c0-118">Windows 10 Preview Build 14383</span></span><br/>                                    |
| <span data-ttu-id="276c0-119">標頭</span><span class="sxs-lookup"><span data-stu-id="276c0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="276c0-120"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="276c0-120"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="276c0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="276c0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276c0-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="276c0-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="276c0-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="276c0-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="276c0-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="276c0-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="276c0-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="276c0-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




