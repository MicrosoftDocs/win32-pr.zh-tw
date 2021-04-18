---
description: 使用 Windows 映像取得 (WIA) 服務的第一個步驟是，如果您要針對 Windows XP 或) 更早版本進行程式設計，請 (取得 IWiaDevMgr 介面指標，如果您是針對 Windows Vista 或更新版本的程式設計，則為 IWiaDevMgr2 介面指標 (。
ms.assetid: 8f20c64a-db79-4c3c-a544-685ed82143bb
title: 建立 WIA 裝置管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e315939566eea6fe8a4acabeb5fd8afe247c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989418"
---
# <a name="creating-a-wia-device-manager"></a>建立 WIA 裝置管理員

使用 Windows 映像取得 (WIA) 服務的第一個步驟是，如果您要針對 Windows XP 或) 更早版本進行程式設計，請 (取得 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 介面指標，如果您是針對 windows Vista 或更新版本的程式設計，則為 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) 介面指標 (。 若要這樣做，請使用適當的參數呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 。 範例應用程式 WiaSSamp 會在由下列程式碼所執行的全域函式內建立裝置管理員：


```
    HRESULT CreateWiaDeviceManager( IWiaDevMgr **ppWiaDevMgr ) //XP or earlier
    HRESULT CreateWiaDeviceManager( IWiaDevMgr2 **ppWiaDevMgr ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == ppWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevMgr = NULL;

        //
        // Create an instance of the device manager
        //
        
        //XP or earlier:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr, (void**)ppWiaDevMgr );

        //Vista or later:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr2, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr2, (void**)ppWiaDevMgr ); 

        //
        // Return the result of creating the device manager
        //
        return hr;
    }
```



在此範例中，CLSID \_ WiaDevMgr 和 IID \_ IWiaDevMgr 分別是表示類別識別碼和 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)介面識別碼的 WIA 常數。 CLSID \_ WiaDevMgr2 和 IID \_ IWiaDevMgr2 分別是表示類別識別碼和 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)介面識別碼的 WIA 常數。

[CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)呼叫的 *dwClsCoNtext* 引數值必須是 CLSCTX \_ 本地 \_ 伺服器。 不支援其他伺服器類型，而且元件物件模型 (COM) 會拒絕此參數的任何其他值。

 

 
