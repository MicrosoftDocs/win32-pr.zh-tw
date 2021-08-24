---
description: 根據安裝的作業系統而定，Direct3D 9 API 會在 Windows XP 顯示驅動程式模型 () 或 Windows Vista 顯示驅動程式模型 (WDDM) 上運作。
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM 和 WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0332198cd7c9425a3b5a107259dda1b1e974a04a2379244cdf939384260a89f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746048"
---
# <a name="xpdm-vs-wddm"></a>XPDM 和 WDDM

根據安裝的作業系統而定，Direct3D 9 API 會在 Windows XP 顯示驅動程式模型 () 或 Windows Vista 顯示驅動程式模型 (WDDM) 上運作。 Direct3D API 在兩個驅動程式模型上的運作方式有一些差異。

-   [安全桌面](#secure-desktop)
-   [遠端桌面](#remote-desktop)
-   [Windows 服務](#windows-service)
-   [相關主題](#related-topics)

## <a name="secure-desktop"></a>安全桌面

只要發生下列任何一種情況，安全桌面就會處於作用中狀態：使用者會鎖定其桌面 (Windows + L) 、螢幕保護裝置會在沒有使用者登入) 時啟用 (，或是在使用者帳戶控制顯示提示時預設為啟用。 當安全桌面處於作用中狀態時，就無法存取 HAL 裝置。

XPDM 和 WDDM 之間的差異：

- 嘗試建立 Direct3D9 的 HAL 裝置會失敗 (**D3DERR \_ 無法 \_ 使用**) ，而且任何現有的 Direct3D 9 裝置都會指出目前遺失的裝置傳回碼。

- Direct3D9Ex 和 Direct3D 10 Api 可以在安全桌面啟用時成功建立裝置，而且任何 ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) 或 DXGI) 的呼叫都會傳回狀態碼，指出桌面目前無法使用。



 

## <a name="remote-desktop"></a>遠端桌面

當遠端桌面處於作用中狀態時，顯示電腦會透過網路傳送資訊給主控電腦來處理。

XPDM 和 WDDM 之間的差異：

- 在 XPDM 上，在遠端桌面上建立 Direct3D 9 裝置的所有嘗試都將失敗。

- 在 WDDM 中，遠端桌面支援透過遠端桌面會話建立 HAL 裝置。



 

## <a name="windows-service"></a>Windows 服務

Windows 服務是在背景中執行的處理常式，由服務控制管理員 (SCM) 控制。 服務會獨立于作用中的桌面執行，因此與使用者互動的能力有限。

XPDM 和 WDDM 之間的差異：

- 在 WDDM 上，「會話0隔離」可確保服務無法存取任何使用者桌面做為安全性措施，因此，Windows 服務永遠不會提供 Direct3D 9 HAL 裝置。



 

> [!Note]  
> 您無法在 Windows 服務中使用 Direct3D 9。 如需詳細資訊，請參閱 [Microsoft 支援文章 978635](https://support.microsoft.com/kb/978635)。

 


下表摘要說明此處所列的差異。



| 安全桌面 | XPDM | WDDM (Direct3D9)  | WDDM (Direct3D9Ex/Direct3D10)  |
|-----------------|------|------------------|------------------------------|
| NullREF         | 是  | 是              | 是                          |
| HAL             | 否   | 否               | 是                          |
| REF             | 是  | 是              | 是                          |
| 遠端桌面  |      |                  |                              |
| NullREF         | 否   | 是              | 是                          |
| HAL             | 否   | 是              | 是                          |
| REF             | 是  | 是              | 是                          |
| Windows 服務 |      |                  |                              |
| NullREF         | 否   | 否               | 否                           |
| HAL             | 否   | 否               | 否                           |
| REF             | 否   | 否               | 否                           |
| WARP10          | N/A  | N/A              | 是                          |



 

如需有關 XPDM、WDDM、Direct3D9Ex 和 Direct3D 10 的詳細資訊，請參閱[Windows 中的圖形 api](../direct3darticles/graphics-apis-in-windows-vista.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 裝置](direct3d-devices.md)
</dt> </dl>

 

 
