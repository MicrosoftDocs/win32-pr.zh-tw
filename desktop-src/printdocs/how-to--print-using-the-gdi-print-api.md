---
description: 本主題將介紹如何使用 GDI&160，從原生 Windows 程式進行列印 \# ;列印&\# 160;API。
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 如何：使用 GDI 列印 API 進行列印
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19832ef93a80cc537d16136ac751cb20fd8664d7d1d31d295568de68d6dd846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091928"
---
# <a name="how-to-print-using-the-gdi-print-api"></a>如何：使用 GDI 列印 API 進行列印

本主題介紹如何使用[GDI 列印 API](gdi-printing.md)，從原生 Windows 程式進行列印。

## <a name="overview"></a>概觀

列印通常是原生 Windows 程式不可或缺的一部分，因此它不是您在撰寫程式之後可以輕鬆新增的功能。 針對 Windows 7 設計程式時，您應該考慮使用[XPS 列印 API](xps-printing.md)來提供列印功能，因為它會為未來提供最高的相容性。 必須在 Windows Vista 與舊版 Windows 上執行的程式，很可能會使用[GDI 列印 API](gdi-printing.md)來提供列印功能。 Windows 7 也支援 GDI 列印 api，但它比 XPS 列印 api 更受限制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用列印](using-printing.md)
</dt> <dt>

[如何從 Windows 應用程式列印](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



