---
title: 修改 Wizard 產生的程式碼
description: 修改 Wizard 產生的程式碼
ms.assetid: 391a7773-c3e2-499a-bb63-e5934537d963
keywords:
- Windows Media Player 行動裝置、外掛程式
- Windows Media Player 行動裝置、使用者介面外掛程式
- Windows Media Player Mobile 外掛程式
- 外掛程式，使用者介面
- 外掛程式，Windows Media Player Mobile
- 使用者介面外掛程式，Windows Media Player Mobile
- UI 外掛程式，Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83bda7cb265d0c2e039ada6d9d827c6da3faf63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967214"
---
# <a name="modifying-wizard-generated-code"></a>修改 Wizard 產生的程式碼

在嚮導產生的外掛程式程式碼中，您必須先修改數個位置，您的外掛程式才能使用 Windows Media Player 10 行動裝置版。 在下列範例中，您必須修改的程式碼為粗體。

## <a name="changes-to-wmpplugh"></a>變更為 wmpplug。h

執行 Windows CE 的裝置不支援 ANSI 方法，因此您必須修改 wmpplug 中的 wizard 所產生的下列 ANSI 方法：


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageA( "WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



如下所示修改它，使它變成 Unicode 方法：


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageW( L"WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



## <a name="changes-to-networkpluginh"></a>變更為 NetworkPlugin。h

在 NetworkPlugin 中尋找下列程式碼：


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    COM_INTERFACE(IWMPPluginUI)
END_COM_MAP()
```



修改程式碼，使其看起來像這樣：


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    
COM_INTERFACE_ENTRY_IID(__uuidof(IWMPPluginUI), IWMPPluginUI)
END_COM_MAP()
```



## <a name="changes-to-networkplugindllcpp"></a>變更為 NetworkPlugindll .cpp

在 NetworkPlugindll 中尋找 **DllMain** 函數：


```C++
extern "C" BOOL WINAPI DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, hInstance);
        DisableThreadLibraryCalls(hInstance);
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



修改程式碼，使其看起來像這樣：


```C++
extern "C" BOOL WINAPI DllMain(HANDLE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, (HINSTANCE)hInstance);
#ifndef UNDER_CE
        DisableThreadLibraryCalls((HINSTANCE)hInstance);
#endif
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



## <a name="changes-to-networkplugincpp"></a>變更為 NetworkPlugin .cpp

在 NetworkPlugin 中找出下列程式碼：


```C++
hr = m_spCore->QueryInterface(&spConnectionContainer);
```



修改程式碼，使其看起來像這樣：


```C++
hr = m_spCore->QueryInterface(__uuidof(IConnectionPointContainer), (void**)&spConnectionContainer);
```



## <a name="change-the-threading-model"></a>變更執行緒模型

不同于 Windows 的 ATL，適用于 Windows CE 的 ATL 不支援單元執行緒模型，因為在單一線程和自由執行緒模型的情況下，單元模型需要更多記憶體資源。 因此，您必須在 Stdafx.h .h 和 NetworkPlugin 中尋找所有單元執行緒的實例，並加以變更以表示可用執行緒。

此外，您只能從建立它的執行緒呼叫 Windows Media Player 10 行動裝置控制項。

## <a name="build-and-test-the-project"></a>建立和測試專案

進行這些變更之後，您可以建立您的專案，以確認它在新增任何自訂程式碼之前會先進行編譯。

1.  將作用中的專案設定設為 Win32 (WCE ARMV4) Debug 或 Win32 (WCE ARMV4) 版本。
2.  將使用中平臺設定為 [Pocket PC 2003]。
3.  按一下 [ **組建** ] 功能表項目，然後選取 [ **建立 NetworkPlugin.dll**]。 它應該會在您的裝置上進行編譯、下載及註冊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows Media Player 10 行動裝置版的消費者介面外掛程式**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> </dl>

 

 




