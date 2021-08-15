---
description: DEP/NX 相容性
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: DEP/NX 相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65af83e43defb5216b176755dbc8f32067f907620bc120a16aff8b6db3392c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329623"
---
# <a name="depnx-compatibility"></a>DEP/NX 相容性

根據預設，在 Windows Internet Explorer 7 中，由於相容性的緣故，已停用 DEP/NX。 有幾個熱門的附加元件與 dep/nx 不相容，而且當 Windows Internet Explorer 在啟用 dep/nx 時載入它們時，會失敗。

這些附加元件通常是使用舊版 ATL framework 所建立。 ATL 7.1 及更早版本不是使用 DEP 安全性功能所設計。 幸運的是，Microsoft Windows service pack 的新版本有新的 dep/nx api，可讓您使用 dep/nx，並保有與舊版 ATL 的相容性。 這些新的 Api 可讓 Internet Explorer 加入宣告 DEP/NX，而不會導致使用較舊版本的 ATL 建立的附加元件失敗。

當附加元件不是 DEP/NX 相容且未使用過期的 ATL 時，您可以使用群組原則選項來退出宣告 DEP/Internet Explorer NX，直到部署中斷控制項的更新版本為止。 本機系統管理員可以藉由以系統管理員身分執行 Internet Explorer，並在 [**網際網路選項**] 的 [ **Advanced** ] 窗格中清除 [**啟用記憶體保護**] 選項，以控制 DEP/NX。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
