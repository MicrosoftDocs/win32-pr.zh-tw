---
title: 如何使用裝置存取 API
description: 本主題包含使用裝置存取 API 的工作和設計考慮。
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: bd1ddf9d2716cd01ab2db8acb08d2793a6831ffa6f20aa2c75378f72932d992b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635298"
---
# <a name="how-to-use-the-device-access-api"></a>如何使用裝置存取 API

本主題包含使用裝置存取 API 的工作和設計考慮。

## <a name="steps"></a>步驟

| 主題 | 描述 |
|---|---|
| [自訂裝置的設計考慮](design.md)<br/> | 本主題說明可協助您判斷裝置是否需要自訂驅動程式的設計考慮。<br/> |
| [執行裝置存取物件](create-the-device-access-object.md)<br/> | 本主題說明如何將裝置存取物件具現化，並使用它來存取裝置。 <br/>  |
| [宣告裝置功能](declaring-the-device-capability.md)<br/> | 本主題說明如何宣告裝置功能 GUID。<br/> |
| [將裝置介面註冊為受特殊許可權的應用程式限制](register-the-device-interface-class-as-privileged.md)<br/> | 本主題說明如何新增 **受限制** 的屬性，指出只有特殊許可權的應用程式可以存取裝置介面類別別。<br/> |
| [建立 Windows 執行階段擴充功能](create-a-windows-runtime-extension.md)<br/> | 您可以建立 Windows 執行階段元件包裝存取您驅動程式的元件。 然後，您可以使用 c # 或 JavaScript 為裝置撰寫 Windows 存放區裝置應用程式。<br/> |

## <a name="additional-resources"></a>其他資源

- [自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)示範如何使用裝置存取 api，從 Windows Store 裝置應用程式存取自訂驅動程式。
- [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)會提供資源，以深入瞭解如何設計和開發專用裝置的 Windows 存放裝置應用程式。
- [硬體開發人員中心](/windows-hardware/drivers/)提供適用于所有裝置類型之 Windows 儲存裝置應用程式開發工作的一般資源。
