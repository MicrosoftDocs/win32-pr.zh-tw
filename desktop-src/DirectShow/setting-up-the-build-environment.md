---
description: 打造 DirectShow 應用程式
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: 打造 DirectShow 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972296"
---
# <a name="building-directshow-applications"></a>打造 DirectShow 應用程式

本主題說明建立 DirectShow 應用程式所需的標頭和程式庫。

[Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx)中提供最新的 DirectShow 標頭和程式庫。

## <a name="header-files"></a>標頭檔

所有的 DirectShow 應用程式都會使用下表所示的標頭檔。



| 標頭檔案 | 需要                 |
|-------------|------------------------------|
| Dshow。h     | 所有的 DirectShow 應用程式。 |



 

某些 DirectShow 介面需要額外的標頭檔。 這些需求會在介面參考中注明。

## <a name="library-files"></a>程式庫檔案

DirectShow 使用下表所示的靜態程式庫檔案。



| 程式庫檔案 | Description                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| Strmiids .lib |  (Clsid) 和介面識別碼匯出類別識別碼 (Iid) 。                                                           |
| Quartz .lib   | 匯出 [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) 函數。 如果您未呼叫此函式，則不需要此程式庫。 |



 

針對 debug 和 release 組建使用相同的 .lib 檔案。

## <a name="filter-base-classes"></a>篩選基類

Windows SDK 提供一組 c + + 類別，如果您要撰寫自訂的 DirectShow 篩選器，則建議使用這組類別。 這些類別會以範例程式碼的形式提供，您可以將其編譯成靜態程式庫。 如需詳細資訊，請參閱 [DirectShow 基類](directshow-base-classes.md)。

## <a name="redistributable-dlls"></a>可轉散發 Dll

針對 Windows XP Service Pack 2 (SP2) 和更新版本所撰寫的 DirectShow 應用程式不需要轉散發任何 DirectShow Dll。

若為 Windows XP Service Pack 1 (SP1) 及更早版本，可從 Microsoft DirectX SDK 取得可轉散發的 DirectShow Dll。 這些 Dll 的最新版本是9.0 版 c。 不打算進一步開發這些可轉散發 Dll。 Windows XP Service Pack 2 (SP2) 包含9.0 版的 c Dll。

Redstributable 套件包含下列 Dll：

-   dxnt.cab
    -   amstream.dll
    -   devenum.dll
    -   encapi.dll
    -   ks.sys
    -   ksolay.ax
    -   ksproxy.ax
    -   ksuser.dll
    -   l3codecx.ax
    -   mciqtz32.dll
    -   mpg2splt.ax
    -   msdmo.dll
    -   mskssrv.sys
    -   mspclock.sys
    -   mspqm.sys
    -   mstee.sys
    -   mswebdvd.dll
    -   qasf.dll
    -   qcap.dll
    -   qdv.dll
    -   qdvd.dll
    -   qedit.dll
    -   qedwipes.dll
    -   quartz.dll
    -   stream.sys
    -   swenum.sys
-   bda.cab
    -   bdaplgin.ax
    -   bdasup.sys
    -   ccdecode.sys
    -   ipsink.ax
    -   kstvtune.ax
    -   kswdmcap.ax
    -   ksxbar.ax
    -   mpe.sys
    -   mpeg2data.ax
    -   msdv.sys
    -   msdvbnp.ax
    -   msvidctl.dll
    -   msyuv.dll
    -   nabtsfec.sys
    -   ndisip.sys
    -   psisdecd.dll
    -   psisrndr.ax
    -   slip.sys
    -   streamip.sys
    -   vbisurf.ax
    -   wstcodec.sys
    -   wstdecod.dll

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 DirectShow 篩選器](building-directshow-filters.md)
</dt> </dl>

 

 
