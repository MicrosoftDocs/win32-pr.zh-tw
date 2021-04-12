---
description: Direct3D 裝置管理員
ms.assetid: d82fd82d-510e-4004-b18b-8f2372e29701
title: Direct3D 裝置管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aeff41b790df9537854ab715724d95cee646168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317979"
---
# <a name="direct3d-device-manager"></a><span data-ttu-id="55cef-103">Direct3D 裝置管理員</span><span class="sxs-lookup"><span data-stu-id="55cef-103">Direct3D Device Manager</span></span>

<span data-ttu-id="55cef-104">Microsoft Direct3D 裝置管理員可讓兩個或多個物件共用相同的 Microsoft Direct3D 9 裝置。</span><span class="sxs-lookup"><span data-stu-id="55cef-104">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span> <span data-ttu-id="55cef-105">一個物件會作為 Direct3D 9 裝置的擁有者。</span><span class="sxs-lookup"><span data-stu-id="55cef-105">One object acts as the owner of the Direct3D 9 device.</span></span> <span data-ttu-id="55cef-106">若要共用裝置，裝置的擁有者會建立 Direct3D 裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="55cef-106">To share the device, the owner of the device creates the Direct3D device manager.</span></span> <span data-ttu-id="55cef-107">其他物件可以從裝置擁有者取得裝置管理員的指標，然後使用 [裝置管理員] 取得 Direct3D 裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="55cef-107">Other objects can obtain a pointer to the device manager from the device owner, then use the device manager to get a pointer to the Direct3D device.</span></span> <span data-ttu-id="55cef-108">任何使用裝置的物件都會保存獨佔鎖定，以防止其他物件同時使用該裝置。</span><span class="sxs-lookup"><span data-stu-id="55cef-108">Any object that uses the device holds an exclusive lock, which prevents other objects from using the device at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="55cef-109">Direct3D 裝置管理員只支援 Direct3D 9 裝置。</span><span class="sxs-lookup"><span data-stu-id="55cef-109">The Direct3D Device Manager supports Direct3D 9 devices only.</span></span> <span data-ttu-id="55cef-110">它不支援 DXGI 裝置。</span><span class="sxs-lookup"><span data-stu-id="55cef-110">It does not support DXGI devices.</span></span>

 

<span data-ttu-id="55cef-111">若要建立 Direct3D 裝置管理員，請呼叫 [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)。</span><span class="sxs-lookup"><span data-stu-id="55cef-111">To create the Direct3D device manager, call [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span> <span data-ttu-id="55cef-112">此函式會傳回裝置管理員 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標，以及重設權杖。</span><span class="sxs-lookup"><span data-stu-id="55cef-112">This function returns a pointer to the device manager's [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface, along with a reset token.</span></span> <span data-ttu-id="55cef-113">重設權杖可讓 Direct3D 裝置的擁有者在裝置管理員上設定裝置)  (和重設。</span><span class="sxs-lookup"><span data-stu-id="55cef-113">The reset token enables the owner of the Direct3D device to set (and reset) the device on the device manager.</span></span> <span data-ttu-id="55cef-114">若要初始化裝置管理員，請呼叫 [**IDirect3DDeviceManager9：： ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)。</span><span class="sxs-lookup"><span data-stu-id="55cef-114">To initialize the device manager, call [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span> <span data-ttu-id="55cef-115">傳入 Direct3D 裝置的指標，以及重設權杖。</span><span class="sxs-lookup"><span data-stu-id="55cef-115">Pass in a pointer to the Direct3D device, along with the reset token.</span></span>

<span data-ttu-id="55cef-116">下列程式碼說明如何建立和初始化裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="55cef-116">The following code shows how to create and initialize the device manager.</span></span>


```C++
HRESULT CreateD3DDeviceManager(
    IDirect3DDevice9 *pDevice, 
    UINT *pReset, 
    IDirect3DDeviceManager9 **ppManager
    )
{
    UINT resetToken = 0;

    IDirect3DDeviceManager9 *pD3DManager = NULL;

    HRESULT hr = DXVA2CreateDirect3DDeviceManager9(&resetToken, &pD3DManager);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pD3DManager->ResetDevice(pDevice, resetToken);

    if (FAILED(hr))
    {
        goto done;
    }

    *ppManager = pD3DManager;
    (*ppManager)->AddRef();

    *pReset = resetToken;


done:
    SafeRelease(&pD3DManager);
    return hr;
}
```



<span data-ttu-id="55cef-117">裝置擁有者必須提供方法，讓其他物件取得 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="55cef-117">The device owner must provide a way for other objects to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="55cef-118">標準機制是執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。</span><span class="sxs-lookup"><span data-stu-id="55cef-118">The standard mechanism is to implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="55cef-119">服務 GUID 是 MR \_ 影片 \_ 加速 \_ 服務。</span><span class="sxs-lookup"><span data-stu-id="55cef-119">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="55cef-120">若要在數個物件之間共用裝置，每個物件 (包括裝置的擁有者) 必須透過 [裝置管理員] 存取裝置，如下所示：</span><span class="sxs-lookup"><span data-stu-id="55cef-120">To share the device among several objects, each object (including the owner of the device) must access the device through the device manager, as follows:</span></span>

1.  <span data-ttu-id="55cef-121">呼叫 [**IDirect3DDeviceManager9：： OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) 來取得裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="55cef-121">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the device.</span></span>
2.  <span data-ttu-id="55cef-122">若要使用裝置，請呼叫 [**IDirect3DDeviceManager9：： LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) ，並傳入裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="55cef-122">To use the device, call [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) and pass in the device handle.</span></span> <span data-ttu-id="55cef-123">方法會傳回 **IDirect3DDevice9** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="55cef-123">The method returns a pointer to the **IDirect3DDevice9** interface.</span></span> <span data-ttu-id="55cef-124">您可以根據 *fBlock* 參數的值，以封鎖模式或非封鎖模式來呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="55cef-124">The method can be called in a blocking mode or a non-blocking mode, depending on the value of the *fBlock* parameter.</span></span>
3.  <span data-ttu-id="55cef-125">當您使用完裝置時，請呼叫 [**IDirect3DDeviceManager9：： UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice)。</span><span class="sxs-lookup"><span data-stu-id="55cef-125">When you are done using the device, call [**IDirect3DDeviceManager9::UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span></span> <span data-ttu-id="55cef-126">此方法可將裝置提供給其他物件。</span><span class="sxs-lookup"><span data-stu-id="55cef-126">This method makes the device available to other objects.</span></span>
4.  <span data-ttu-id="55cef-127">在結束之前，請呼叫 [**IDirect3DDeviceManager9：： CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) 來關閉裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="55cef-127">Before exiting, call [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) to close the device handle.</span></span>

<span data-ttu-id="55cef-128">您應該只在使用裝置時保留裝置鎖定，因為持有裝置鎖定可防止其他物件使用該裝置。</span><span class="sxs-lookup"><span data-stu-id="55cef-128">You should hold the device lock only while using the device, because holding the device lock prevents other objects from using the device.</span></span>

<span data-ttu-id="55cef-129">裝置的擁有者可以藉由呼叫 [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)，隨時切換到其他裝置，通常是因為原始裝置已遺失。</span><span class="sxs-lookup"><span data-stu-id="55cef-129">The owner of the device can switch to another device at any time by calling [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), typically because the original device was lost.</span></span> <span data-ttu-id="55cef-130">裝置遺失的原因可能有許多種，包括監視器解析度的變更、電源管理動作、鎖定和解除鎖定電腦等等。</span><span class="sxs-lookup"><span data-stu-id="55cef-130">Device loss can occur for various reasons, including changes in the monitor resolution, power management actions, locking and unlocking the computer, and so forth.</span></span> <span data-ttu-id="55cef-131">如需詳細資訊，請參閱 Direct3D 檔。</span><span class="sxs-lookup"><span data-stu-id="55cef-131">For more information, see the Direct3D documentation.</span></span>

<span data-ttu-id="55cef-132">[**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)方法會讓先前開啟的任何裝置控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="55cef-132">The [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method invalidates any device handles that were opened previously.</span></span> <span data-ttu-id="55cef-133">當裝置控制碼無效時， [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) 方法會傳回 **DXVA2 \_ E \_ 新的 \_ 影片 \_ 裝置**。</span><span class="sxs-lookup"><span data-stu-id="55cef-133">When a device handle is invalid, the [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method returns **DXVA2\_E\_NEW\_VIDEO\_DEVICE**.</span></span> <span data-ttu-id="55cef-134">如果發生這種情況，請關閉控制碼並再次呼叫 [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) ，以取得新的裝置控制碼，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="55cef-134">If this occurs, close the handle and call [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) again to obtain a new device handle, as shown in the following code.</span></span>

<span data-ttu-id="55cef-135">下列範例示範如何開啟裝置控制碼並鎖定裝置。</span><span class="sxs-lookup"><span data-stu-id="55cef-135">The following example shows how to open a device handle and lock the device.</span></span>


```C++
HRESULT LockDevice(
    IDirect3DDeviceManager9 *pDeviceManager,
    BOOL fBlock,
    IDirect3DDevice9 **ppDevice, // Receives a pointer to the device.
    HANDLE *pHandle              // Receives a device handle.   
    )
{
    *pHandle = NULL;
    *ppDevice = NULL;

    HANDLE hDevice = 0;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);

    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->LockDevice(hDevice, ppDevice, fBlock);
    }

    if (hr == DXVA2_E_NEW_VIDEO_DEVICE)
    {
        // Invalid device handle. Try to open a new device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->OpenDeviceHandle(&hDevice);
        }

        // Try to lock the device again.
        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->LockDevice(hDevice, ppDevice, TRUE); 
        }
    }

    if (SUCCEEDED(hr))
    {
        *pHandle = hDevice;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="55cef-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="55cef-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55cef-137">DirectX Video 加速2。0</span><span class="sxs-lookup"><span data-stu-id="55cef-137">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



