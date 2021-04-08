---
description: 傘程式庫是單一的靜態程式庫，可匯出 Win32 Api 的子集。 例如，名為 OneCore 的傘程式庫會針對所有 Windows 10 裝置通用的 Win32 Api 子集提供匯出。
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Windows 傘程式庫
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 86a8f9b8f3bef5081bd7e0e64300b9295fd85401
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2020
ms.locfileid: "103684228"
---
# <a name="windows-umbrella-libraries"></a>Windows 傘程式庫

*傘* 程式庫是單一的靜態程式庫，可匯出 Win32 api 的子集。 例如，名為 OneCore 的傘程式庫會針對所有 Windows 10 裝置通用的 Win32 Api 子集提供匯出 **。**

階層程式庫中的 Api 可以跨各種不同的模組來執行 (無論是) 的 [api 集](windows-apisets.md) 或 DLL，但階層程式庫會將該詳細資料抽象化，讓您的應用程式在作業系統版本之間更具可攜性。 只要將您的桌面應用程式或驅動程式連結到包含您感興趣之 Api 集合的包含您感興趣的 Api 集，就可以完成這項作業。 

| 程式庫 | 描述 |
|------------------------|-------------------------|
| OneCore .lib | 此程式庫會針對所有 Windows 10 裝置通用的 Win32 Api 子集提供匯出。 將您的桌面應用程式或驅動程式與 OneCore 連結 (，且沒有任何其他程式庫) 存取這些 Api。 如果您將應用程式或驅動程式連結至 OneCore，而您只呼叫該程式庫中的 Win32 Api，則您的應用程式或驅動程式將會在所有 Windows 10 裝置上順利載入。         |
| OneCore_apiset .lib | 此程式庫提供與 OneCore 相同的涵蓋範圍，但使用 [API 集直接轉送](api-set-loader-operation.md#direct-forwarding)。 請注意，使用此程式庫只會與您設為目標的 SDK 版本或更高版本所指定的 Windows 10 版本相容。  |
| OneCoreUap .lib | 此程式庫會針對所有支援 Windows 執行階段 (WinRT) 的 Windows 10 裝置，提供通用的 Win32 Api 子集匯出。 將您的桌面應用程式或驅動程式與 OneCoreUap 連結 (，且沒有任何其他程式庫) 存取這些 Api。 如果您將應用程式或驅動程式連結至 OneCoreUap，而您只呼叫該程式庫中的 Win32 Api，則您的應用程式或驅動程式將會在所有支援 UWP 的 Windows 10 裝置上順利載入。 |
| OneCoreUAP_apiset .lib | 此程式庫提供與 OneCoreUAP 相同的涵蓋範圍，但使用 [API 設定的直接轉送](api-set-loader-operation.md#direct-forwarding) 技術。 請注意，使用此程式庫只會與您目標 SDK 所指定或更高版本的 Windows 10 版本相容。  |
