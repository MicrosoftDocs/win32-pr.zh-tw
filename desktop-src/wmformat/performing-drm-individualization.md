---
title: 執行 DRM 的個人化
description: 執行 DRM 的個人化
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows媒體格式 SDK，DRM 用戶端擴充 Api
- Windows媒體格式 SDK，用戶端擴充 Api
- Windows媒體格式 SDK，擴充的 Api
- Windows媒體格式 SDK，Api
- 'Windows媒體格式 SDK、數位版權管理 (DRM) '
- Windows媒體格式 SDK，DRM 的個人化
- Windows媒體格式 SDK，個人化
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) 、個人化
- DRM (數位版權管理) 、個人化
- 數位版權管理 (DRM) ，DRM 的個人化
- DRM (數位版權管理) ，DRM 的個人化
- DRM 用戶端擴充 Api，個人化
- 用戶端擴充 Api，個人化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c46d2cd6fccd2c6c1a8898a2d0215b6bc62a3655b12412192d1809021747ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027386"
---
# <a name="performing-drm-individualization"></a>執行 DRM 的個人化

「個人化」是在用戶端電腦上更新 DRM 元件、將其加密以及使其成為唯一的程式。 當電腦是個人化的時，DRM 元件會系結至電腦，而且無法在任何其他電腦上將內容解碼。 Windows 媒體 DRM 用戶端擴充 api 提供在用戶端電腦上 individualizing DRM 元件的支援。

藉由呼叫 [**IWMDRMSecurity：:P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) 方法來執行個人化。 您可以呼叫 **PerformSecurityUpdate** ，只有當伺服器上的版本比用戶端電腦上安裝的版本還要新時，才會賦予，或者，您可以在不考慮相對安全性版本的情況下強制執行個人化。 視需要的個人化旗標是 WMDRM \_ 安全性 \_ 執行 \_ INDIV。 強制執行的個人化旗標為 WMDRM \_ 安全性 \_ 執行 \_ 強制 \_ INDIV。

**PerformSecurityUpdate** 是非同步呼叫。 它會快速傳回，然後產生事件，以提供有關「個人化」程式的狀態資訊。 大部分產生的事件將會是 **MEWMDRMIndividualizationProgress** 事件，每個事件都有相關聯的 [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) 介面。 若要取得狀態介面，您必須呼叫 **IMFMediaEvent：： GetValue** 來取出位於相同物件上的 **IUnknown** 指標，然後查詢它以進行 **IWMDRMIndividualizationStatus**。

您可以藉由呼叫 [**IWMDRMIndividualizeStatus：： GetStatus**](iwmdrmindividualizationstatus-getstatus.md)，取得 [**WM \_ 賦予 \_ 狀態**](drmwm-individualize-status.md)結構的資料。 每個產生的事件都有自己的物件，其狀態為，因此您必須逐一查看取得事件值，並每次查詢狀態介面的流程。

視下載的大小而定，可能會有數十個或數百個 **MEWMDRMIndividualizationProgress** 事件。 當「個人化」程式完成時，就會產生 **MEWMDRMIndividualizationCompleted** 事件。

當個人化完成時，唯一會反映新的個人化狀態的現有物件就是繼承自 [**IWMDRMSecurity**](iwmdrmsecurity.md)的物件。 所有其他現有的物件將不會更新。 您必須釋放並重新建立任何其他物件，使其反映新的個別狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 的個人化範例**](drm-individualization-example.md)
</dt> <dt>

[**程式設計指南**](drm-programming-guide.md)
</dt> <dt>

[**使用媒體基礎事件模型**](using-the-media-foundation-model.md)
</dt> <dt>

[Windows媒體 DRM 的個人化最佳作法](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 




