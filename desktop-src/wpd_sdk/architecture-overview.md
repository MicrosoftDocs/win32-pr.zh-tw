---
description: 架構概觀
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: 架構概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76eafce326655a4d9386d37c02df9ef0ab2b9772b5e87eedaff40a19383b2cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590461"
---
# <a name="architecture-overview"></a>架構概觀

WPD 架構可以分為三個進程。 在這些程式中，WPD 的三個主要元件： API、序列化程式和驅動程式。 下圖說明構成 WPD 架構的處理常式和元件。

![顯示 wpd api、序列化程式和驅動程式元件的圖例](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>WPD 應用程式設計介面

WPD API 會實作為同進程的 COM 伺服器。 API 會使用標準 Microsoft Win32 Api 來與適當的 WPD 驅動程式通訊。 API 物件和驅動程式會使用名為 WPD 序列化程式的元件，將參數封裝或解除封裝至 Windows driver Foundation (WDF) -使用者模式驅動程式架構)  (的的。

## <a name="the-wpd-serializer"></a>WPD 序列化程式

WPD 序列化程式會實作為同進程的 COM 伺服器。 WPD API 會使用序列化程式，將命令和參數封裝至傳送至驅動程式的訊息緩衝區。 驅動程式會使用序列化程式將這些訊息緩衝區解壓縮以進行處理。 驅動程式也會使用序列化程式將資料和參數封裝至傳回給 WPD API 的回應緩衝區，而 WPD API 會使用序列化程式來將這些回應緩衝區解壓縮，以傳回給呼叫端。

## <a name="wpd-driver"></a>WPD 驅動程式

WPD 驅動程式會實作為標準 Windows 驅動程式基礎 (WDF) -使用者模式驅動程式架構)  (的的驅動程式。 WPD 驅動程式是由 UMDF 在稱為驅動程式主機的個別進程中裝載。

驅動程式會接收來自 UMDF 反映程式的訊息 (這不會顯示在圖表中，因為接收緩衝區對驅動程式而言並不重要。 如需) 的詳細資訊，請參閱 UMDF 檔。 驅動程式會執行 WPD 特定的 i/o 控制項程式碼， (IOCL) 處理常式來處理 WPD API 所接收的 WPD 訊息。 驅動程式會使用 WPD 序列化程式，將命令和參數解壓縮至這些訊息緩衝區，並將回應封裝至傳回緩衝區。

WPD 驅動程式可以通過核心模式驅動程式來與其裝置通訊，通常是透過 Win32 檔案作業來存取， (也就是 CreateFile、ReadFile、WriteFile 等) 。 針對常見的匯流排，Microsoft 會提供標準核心驅動程式供廠商使用，這可讓廠商寄送僅限使用者模式的驅動程式解決方案。 此外，對於媒體傳輸通訊協定 (MTP) 和大量儲存體類別 (SERVICES.MSC) 裝置，Microsoft 將提供 WPD 類別的驅動程式。

如需有關 WPD 驅動程式的詳細資訊，請參閱 Windows 驅動程式套件中的 Windows 便攜裝置驅動程式檔集。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式總覽**](application-overview.md)
</dt> </dl>

 

 



