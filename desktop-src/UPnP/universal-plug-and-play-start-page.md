---
title: UPnP API
description: UPnP 架構可啟用智慧型設備、無線裝置及電腦的動態網路功能。
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104093463"
---
# <a name="upnp-apis"></a>UPnP API

## <a name="purpose"></a>目的

UPnP 架構可啟用智慧型設備、無線裝置及電腦的動態網路功能。 有兩個 Api 可搭配使用 UPnP 認證的裝置：

-   控制點 API，由用來尋找及控制裝置的一組 COM 介面所組成。
-   裝置主機 API，包含一組用來執行電腦所裝載之裝置的 COM 介面。

## <a name="where-applicable"></a>適用時

控制點 API 可讓開發人員撰寫應用程式，以搜尋及控制 UPnP 認證的裝置。 裝置主機 API 可讓開發人員執行 UPnP 認證裝置的功能，並使用裝置主機管理 UPnP 認證裝置的探索、描述、控制、簡報和事件功能。

## <a name="developer-audience"></a>開發人員對象

使用控制點 Api 和裝置主機 Api 的開發人員必須熟悉 UPnP 裝置架構。 如需詳細資訊，請參閱 [Upnp 執行檔](https://openconnectivity.org/resources/upnpresources.zip) 和 [upnp 論壇](https://openconnectivity.org/)。

使用裝置主機 Api 的開發人員應該熟悉 Active Template Library (ATL) 和 COM 介面。

控制點 Api 和裝置主機 Api 是由各種應用程式所使用，從 HTML 網頁中內嵌的腳本到完備的 c + + 和 Microsoft Visual Basic 程式。

只有控制點 API 支援 Visual Basic Scripting Edition (VBScript) 。

## <a name="run-time-requirements"></a>執行階段需求求

控制點 API 是在執行 Microsoft Windows Millennium Edition、Windows XP、Windows XP Professional 和 Windows CE .NET 的電腦上使用。

裝置主機 API 是在執行 Windows XP、Windows XP Professional 和 Windows CE .NET 的電腦上使用。

如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的「需求」。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                          | 描述                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [UPnP 架構總覽](overview-of-universal-plug-and-play.md)<br/>            | 一般資訊和背景。<br/>                                                     |
| [控制點總覽](control-point-api.md)<br/>                                     | 指向控制點 API 的一般資訊。<br/>                                        |
| [使用控制點 API](using-the-control-point-api-with-upnp-technology.md)<br/> | 示範如何開發可控制 UPnP 認證裝置之應用程式的範例程式碼。<br/> |
| [控制點 API 參考](control-point-api-with-upnp-technology-reference.md)<br/> | 控制點元件介面、方法和事件的檔。<br/>               |
| [裝置主機 API 總覽](device-host-api.md)<br/>                                     | 裝置主機 API 的一般資訊。<br/>                                          |
| [使用裝置主機 API](using-the-device-host-api-with-upnp-technology.md)<br/>     | 示範如何針對 UPnP 認證的裝置開發應用程式的範例程式碼。<br/>        |
| [裝置主機 API 參考](device-host-api-with-upnp-technology-reference.md)<br/>     | 裝置主機元件介面、方法和事件的檔。<br/>                 |



 

 

 





