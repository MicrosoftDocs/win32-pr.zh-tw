---
title: Windows Vista 的新功能
description: 映射色彩管理的版本 1.0 (ICM) 已在 Microsoft Windows 95 中提供，並在 Windows 裝置內容中提供基本的色彩管理功能。
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows Color System (WCS) ，Windows Vista
- WCS (Windows Color System) ，Windows Vista
- 影像色彩管理，Windows Vista
- 色彩管理，Windows Vista
- 色彩，Windows Vista
- Windows Color System (WCS) ，作業系統
- WCS (Windows 色彩系統) ，作業系統
- 影像色彩管理，作業系統
- 色彩管理，作業系統
- 色彩，作業系統
- 影像色彩管理 (ICM)
- 'ICM (影像色彩管理) '
- Windows Vista 色彩管理
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106997592"
---
# <a name="whats-new-in-windows-vista"></a>Windows Vista 的新功能

映射色彩管理的版本 1.0 (ICM) 已在 Microsoft Windows 95 中提供，並在 Windows 裝置內容中提供基本的色彩管理功能。

ICM 版本2.0 已在 Windows 98、Windows Millennium Edition、Windows 2000 和 WindowsXP 中提供，並包含各種在裝置內容以外實行色彩管理的新功能。 這些新函式適用于需求較高的色彩管理需求，並讓應用程式能更充分掌控色彩管理進程。

隨著 Windows Vista 的發行，ICM 2.0 現在已包含在 Windows Color System (WCS) 1.0，這會增加更多功能。 下表列出新的應用程式開發介面 (API) 隨附于 Windows Vista 中。

## <a name="new-api-shipping-in-windows-vista"></a>Windows Vista 中的新 API 傳送



列舉

API 名稱

標頭

程式庫

[**COLORDATATYPE**](/windows/win32/api/icm/ne-icm-colordatatype)

icm。h

mscms .lib

[**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

icm。h

mscms .lib

[**COLORPROFILETYPE**](/windows/win32/api/icm/ne-icm-colorprofiletype)

icm。h

mscms .lib

[**WCS \_ 設定檔 \_ 管理 \_ 範圍**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

icm。h

mscms .lib



 



函式

API 名稱

標頭

程式庫

[**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

icm。h

mscms .lib

[**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

icm。h

mscms .lib

[**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

icm。h

mscms .lib

[**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

icm。h

mscms .lib

[**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

icm。h

mscms .lib

[**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

icm。h

mscms .lib

[**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

icm。h

mscms .lib

[**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

icm。h

mscms .lib

[**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

icm。h

mscms .lib

[**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

icm。h

mscms .lib

[**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

icm。h

mscms .lib

[**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

icm。h

mscms .lib

[**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

icm。h

mscms .lib

[**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

icm。h

mscms .lib

[**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

icm。h

mscms .lib



 



介面及其函數

API 名稱

標頭

程式庫

[**IDeviceModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin::ColorimetricToDeviceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin：:D eviceToColorimetricColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin::GetGamutBoundaryMesh**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin::GetGamutBoundaryMeshSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin::GetNeutralAxis**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin::GetNeutralAxisSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin::GetNumChannels**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin::GetPrimarySamples**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin：： Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

WcsPlugIn。h

N/A

[**IDeviceModelPlugin::SetTransformDeviceModelInfo**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

WcsPlugIn。h

N/A

[**IGamutMapModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

WcsPlugIn。h

N/A

[**IGamutMapModelPlugin：： Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

WcsPlugIn。h

N/A

[**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

WcsPlugIn。h

N/A



 



結構

API 名稱

標頭

程式庫

[**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

WcsPlugIn。h

N/A

[**GamutBoundaryDescription**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

WcsPlugIn。h

N/A

[**XYZColorF**](https://www.bing.com/search?q=**XYZColorF**)

WcsPlugIn。h

N/A

[**JChColorF**](https://www.bing.com/search?q=**JChColorF**)

WcsPlugIn。h

N/A

[**JabColorF**](https://www.bing.com/search?q=**JabColorF**)

WcsPlugIn。h

N/A

[**GamutShell**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

WcsPlugIn。h

N/A

[**GamutShellTriangle**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

WcsPlugIn。h

N/A

[**PrimaryJabColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

WcsPlugIn。h

N/A

[**PrimaryXYZColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

WcsPlugIn。h

N/A



 

 

 