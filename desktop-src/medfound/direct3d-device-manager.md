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
# <a name="direct3d-device-manager"></a>Direct3D 裝置管理員

Microsoft Direct3D 裝置管理員可讓兩個或多個物件共用相同的 Microsoft Direct3D 9 裝置。 一個物件會作為 Direct3D 9 裝置的擁有者。 若要共用裝置，裝置的擁有者會建立 Direct3D 裝置管理員。 其他物件可以從裝置擁有者取得裝置管理員的指標，然後使用 [裝置管理員] 取得 Direct3D 裝置的指標。 任何使用裝置的物件都會保存獨佔鎖定，以防止其他物件同時使用該裝置。

> [!Note]  
> Direct3D 裝置管理員只支援 Direct3D 9 裝置。 它不支援 DXGI 裝置。

 

若要建立 Direct3D 裝置管理員，請呼叫 [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)。 此函式會傳回裝置管理員 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標，以及重設權杖。 重設權杖可讓 Direct3D 裝置的擁有者在裝置管理員上設定裝置)  (和重設。 若要初始化裝置管理員，請呼叫 [**IDirect3DDeviceManager9：： ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)。 傳入 Direct3D 裝置的指標，以及重設權杖。

下列程式碼說明如何建立和初始化裝置管理員。


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



裝置擁有者必須提供方法，讓其他物件取得 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標。 標準機制是執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。 服務 GUID 是 MR \_ 影片 \_ 加速 \_ 服務。

若要在數個物件之間共用裝置，每個物件 (包括裝置的擁有者) 必須透過 [裝置管理員] 存取裝置，如下所示：

1.  呼叫 [**IDirect3DDeviceManager9：： OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) 來取得裝置的控制碼。
2.  若要使用裝置，請呼叫 [**IDirect3DDeviceManager9：： LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) ，並傳入裝置控制碼。 方法會傳回 **IDirect3DDevice9** 介面的指標。 您可以根據 *fBlock* 參數的值，以封鎖模式或非封鎖模式來呼叫方法。
3.  當您使用完裝置時，請呼叫 [**IDirect3DDeviceManager9：： UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice)。 此方法可將裝置提供給其他物件。
4.  在結束之前，請呼叫 [**IDirect3DDeviceManager9：： CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) 來關閉裝置控制碼。

您應該只在使用裝置時保留裝置鎖定，因為持有裝置鎖定可防止其他物件使用該裝置。

裝置的擁有者可以藉由呼叫 [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)，隨時切換到其他裝置，通常是因為原始裝置已遺失。 裝置遺失的原因可能有許多種，包括監視器解析度的變更、電源管理動作、鎖定和解除鎖定電腦等等。 如需詳細資訊，請參閱 Direct3D 檔。

[**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)方法會讓先前開啟的任何裝置控制碼失效。 當裝置控制碼無效時， [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) 方法會傳回 **DXVA2 \_ E \_ 新的 \_ 影片 \_ 裝置**。 如果發生這種情況，請關閉控制碼並再次呼叫 [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) ，以取得新的裝置控制碼，如下列程式碼所示。

下列範例示範如何開啟裝置控制碼並鎖定裝置。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



