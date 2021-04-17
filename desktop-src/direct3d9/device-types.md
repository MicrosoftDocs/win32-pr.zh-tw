---
description: " (Direct3D 9) 的裝置類型"
ms.assetid: 860f3de2-beaf-4df1-82d0-a4b7508156c2
title: " (Direct3D 9) 的裝置類型"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84efe80c022403c36e760860893f3619e1c9356
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317627"
---
# <a name="device-types-direct3d-9"></a> (Direct3D 9) 的裝置類型

## <a name="hal-device"></a>HAL 裝置

主要裝置類型是 hal 裝置，其支援硬體加速點陣化，以及硬體和軟體頂點處理。 如果您執行應用程式所在的電腦配備了支援 Direct3D 顯示卡，您的應用程式應該會使用它執行 Direct3D 作業。 Direct3D hal 裝置會實作硬體中的所有或部分轉換、光源和點陣化模組。

應用程式不會直接存取圖形卡。 它們會呼叫 Direct3D 功能和方法。 Direct3D 會透過 hal 存取硬體。 如果您的應用程式執行所在的電腦支援 hal，它使用 hal 裝置將可獲得最佳效能。

若要建立 hal 裝置，請[](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)使用 D3DDEVTYPE \_ hal 作為裝置類型來呼叫 CreateDevice。

## <a name="reference-device"></a>參照裝置

Direct3D 支援額外的裝置類型，稱為參照裝置或軟體模擬轉譯器。 與軟體裝置不同的是，軟體模擬轉譯器支援每一項 Direct3D 功能。 此裝置主要用於偵錯，因此只在已安裝 DirectX SDK 的電腦上提供。 由於這些功能實作的目的在於精確性，而非速度，並且在軟體中實作，因此結果不會非常快。 軟體模擬轉譯器確實會盡可能利用特殊 CPU 指令，但主要不是用於零售應用程式。 僅針對功能測試或展示目的使用軟體模擬轉譯器。 若要建立參考裝置，請[](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)使用 D3DDEVTYPE \_ REF 作為裝置類型來呼叫 CreateDevice 方法。

## <a name="hal-vs-ref-devices"></a>HAL 與參照裝置比較

HAL (硬體抽象層) 裝置和 REF (軟體模擬轉譯器) 裝置是 Direct3D 裝置的主要兩種類型；第一種是以硬體支援為基礎，速度非常快，但可能不會提供全面支援；第二種則不會使用硬體加速，因此非常慢，但是保證支援完整的 Direct3D 功能，並採取正確的方式。 一般來刷，您只會需要使用 HAL 裝置，但是如果您使用某些圖形卡不支援的進階功能，則您可能需要改用 REF。

其他可能想要使用 REF 的情況是，如果 HAL 裝置產生奇怪的結果，也就是說，您確定程式碼是正確的，但結果卻不如預期。 REF 裝置保證會正確運作，因此您可能想要在 REF 裝置上測試應用程式，並查看奇怪的情形是否繼續發生。 如果未繼續發生，表示 (a) 您的應用程式假設圖形卡支援它應該不支援的項目，或 (b) 是驅動程式錯誤。 如果使用 REF 裝置仍然無法運作，表示是應用程式錯誤。

## <a name="hardware-vs-software-vertex-processing"></a>硬體與軟體頂點處理比較

硬體與軟體頂點處理僅適用於 HAL 裝置。 當您透過管線推送頂點時，它們需要轉換 (輪流以世界、檢視、投影矩陣) 和照亮 (藉由 D3D 內建的照明) - 此處理階段稱為 T&L (代表轉換與光源)。 硬體頂點處理表示是在硬體內完成 (如果硬體支援的話)；因此，軟體頂點處理是在軟體內完成。 一般方式是先嘗試建立硬體 T&L 裝置，如果失敗則嘗試混合，再失敗則嘗試軟體。  (如果軟體失敗，則放棄並退出) 錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 裝置](direct3d-devices.md)
</dt> </dl>

 

 
