---
title: WMDM_FORMATCODE 列舉
description: WMDM \_ FORMATCODE 列舉型別會定義格式代碼清單，以說明在裝置上傳送的內容類型。
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- WMDM_FORMATCODE 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_FORMATCODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04db31578f36455fdf77bb4044ad45e5ca9f9a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000660"
---
# <a name="wmdm_formatcode-enumeration"></a><span data-ttu-id="1ccd6-104">WMDM \_ FORMATCODE 列舉</span><span class="sxs-lookup"><span data-stu-id="1ccd6-104">WMDM\_FORMATCODE enumeration</span></span>

<span data-ttu-id="1ccd6-105">**WMDM \_ FORMATCODE** 列舉型別會定義格式代碼清單，以說明在裝置上傳送的內容類型。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-105">The **WMDM\_FORMATCODE** enumeration type defines a list of format codes that describe types of content transferred to and from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ccd6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ccd6-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FORMATCODE { 
  WMDM_FORMATCODE_NOTUSED,
  WMDM_FORMATCODE_ALLIMAGES,
  WMDM_FORMATCODE_UNDEFINED,
  WMDM_FORMATCODE_ASSOCIATION,
  WMDM_FORMATCODE_SCRIPT,
  WMDM_FORMATCODE_EXECUTABLE,
  WMDM_FORMATCODE_TEXT,
  WMDM_FORMATCODE_HTML,
  WMDM_FORMATCODE_DPOF,
  WMDM_FORMATCODE_AIFF,
  WMDM_FORMATCODE_WAVE,
  WMDM_FORMATCODE_MP3,
  WMDM_FORMATCODE_AVI,
  WMDM_FORMATCODE_MPEG,
  WMDM_FORMATCODE_ASF,
  WMDM_FORMATCODE_RESERVED_FIRST,
  WMDM_FORMATCODE_RESERVED_LAST,
  WMDM_FORMATCODE_IMAGE_UNDEFINED,
  WMDM_FORMATCODE_IMAGE_EXIF,
  WMDM_FORMATCODE_IMAGE_TIFFEP,
  WMDM_FORMATCODE_IMAGE_FLASHPIX,
  WMDM_FORMATCODE_IMAGE_BMP,
  WMDM_FORMATCODE_IMAGE_CIFF,
  WMDM_FORMATCODE_IMAGE_GIF,
  WMDM_FORMATCODE_IMAGE_JFIF,
  WMDM_FORMATCODE_IMAGE_PCD,
  WMDM_FORMATCODE_IMAGE_PICT,
  WMDM_FORMATCODE_IMAGE_PNG,
  WMDM_FORMATCODE_IMAGE_TIFF,
  WMDM_FORMATCODE_IMAGE_TIFFIT,
  WMDM_FORMATCODE_IMAGE_JP2,
  WMDM_FORMATCODE_IMAGE_JPX,
  WMDM_FORMATCODE_IMAGE_RESERVED_FIRST,
  WMDM_FORMATCODE_IMAGE_RESERVED_LAST,
  WMDM_FORMATCODE_UNDEFINEDFIRMWARE,
          WMDM_FORMATCODE_WBMP
,
                  WMDM_FORMATCODE_JPEGXR
,
  WMDM_FORMATCODE_WINDOWSIMAGEFORMAT,
  WMDM_FORMATCODE_UNDEFINEDAUDIO,
  WMDM_FORMATCODE_WMA,
  WMDM_FORMATCODE_OGG,
  WMDM_FORMATCODE_AAC,
  WMDM_FORMATCODE_AUDIBLE,
  WMDM_FORMATCODE_FLAC,
          WMDM_FORMATCODE_QCELP
,
          WMDM_FORMATCODE_AMR
,
  WMDM_FORMATCODE_UNDEFINEDVIDEO,
  WMDM_FORMATCODE_WMV,
  WMDM_FORMATCODE_MP4,
  WMDM_FORMATCODE_MP2,
          WMDM_FORMATCODE_3G2
,
                  WMDM_FORMATCODE_AVCHD
,
                  WMDM_FORMATCODE_ATSCTS
,
                          WMDM_FORMATCODE_DVBTS
,
  WMDM_FORMATCODE_UNDEFINEDCOLLECTION,
  WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM,
  WMDM_FORMATCODE_ABSTRACTIMAGEALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOALBUM,
  WMDM_FORMATCODE_ABSTRACTVIDEOALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST,
  WMDM_FORMATCODE_ABSTRACTCONTACTGROUP,
  WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER,
  WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION,
  WMDM_FORMATCODE_WPLPLAYLIST,
  WMDM_FORMATCODE_M3UPLAYLIST,
  WMDM_FORMATCODE_MPLPLAYLIST,
  WMDM_FORMATCODE_ASXPLAYLIST,
  WMDM_FORMATCODE_PLSPLAYLIST,
  WMDM_FORMATCODE_UNDEFINEDDOCUMENT,
  WMDM_FORMATCODE_ABSTRACTDOCUMENT,
  WMDM_FORMATCODE_XMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT,
  WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET,
  WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT,
  WMDM_FORMATCODE_UNDEFINEDMESSAGE,
  WMDM_FORMATCODE_ABSTRACTMESSAGE,
  WMDM_FORMATCODE_UNDEFINEDCONTACT,
  WMDM_FORMATCODE_ABSTRACTCONTACT,
  WMDM_FORMATCODE_VCARD2,
  WMDM_FORMATCODE_VCARD3,
  WMDM_FORMATCODE_UNDEFINEDCALENDARITEM,
  WMDM_FORMATCODE_ABSTRACTCALENDARITEM,
  WMDM_FORMATCODE_VCALENDAR1,
  WMDM_FORMATCODE_VCALENDAR2,
  WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE,
  WMDM_FORMATCODE_MEDIA_CAST,
  WMDM_FORMATCODE_SECTION,
                                  WMDM_FORMATCODE_3G2A

} WMDM_FORMATCODE;
```



## <a name="constants"></a><span data-ttu-id="1ccd6-107">常數</span><span class="sxs-lookup"><span data-stu-id="1ccd6-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1ccd6-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM \_ FORMATCODE \_ NOTUSED**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM\_FORMATCODE\_NOTUSED**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-109">未使用任何格式代碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-109">No format code is used.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM \_ FORMATCODE \_ ALLIMAGES**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM\_FORMATCODE\_ALLIMAGES**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-111">格式化可用於查詢所有影像的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-111">Format code that can be used to query for all images.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**\_ \_ 未定義的 WMDM FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM\_FORMATCODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-113">格式化用來查詢所有未定義物件的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-113">Format code used to query for all undefined objects.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM \_ FORMATCODE \_ 關聯**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM\_FORMATCODE\_ASSOCIATION**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-115">格式化程式碼，用來定義兩個物件之間的連結。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-115">Format code used to define a link between two objects.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM \_ FORMATCODE \_ 腳本**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM\_FORMATCODE\_SCRIPT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-117">格式化腳本檔案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-117">Format code for a script file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM \_ FORMATCODE \_ 可執行檔**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM\_FORMATCODE\_EXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-119">格式化可執行檔的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-119">Format code for an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM \_ FORMATCODE \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM\_FORMATCODE\_TEXT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-121">格式化文字檔的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-121">Format code for a text file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM \_ FORMATCODE \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM\_FORMATCODE\_HTML**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-123">格式化 HTML 檔案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-123">Format code for an HTML file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM \_ FORMATCODE \_ DPOF**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM\_FORMATCODE\_DPOF**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-125">用來表示數位列印順序格式的程式碼格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-125">Format code used to represent the digital print order format.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM \_ FORMATCODE \_ .AIFF**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM\_FORMATCODE\_AIFF**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-127">用來代表音訊交換檔案格式的程式碼格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-127">Format code used to represent the audio interchange file format.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM \_ FORMATCODE \_ WAVE**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM\_FORMATCODE\_WAVE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-129">格式化用於 WAV 檔案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-129">Format code used for a WAV file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM \_ FORMATCODE \_ MP3**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM\_FORMATCODE\_MP3**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-131">格式化用於 MP3 檔案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-131">Format code used for an MP3 file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM \_ FORMATCODE \_ AVI**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM\_FORMATCODE\_AVI**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-133">格式化 AVI 檔案所用的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-133">Format code used for an AVI file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM \_ FORMATCODE \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM\_FORMATCODE\_MPEG**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-135">格式化用於 MPEG 檔案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-135">Format code used for an MPEG file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM \_ FORMATCODE \_ ASF**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM\_FORMATCODE\_ASF**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-137">用來代表 Advanced 系統格式的程式碼 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-137">Format code used to represent an Advanced Systems Format (ASF) file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**\_ \_ 先保留 WMDM \_ FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM\_FORMATCODE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-139">將第一個範圍中的第一個程式碼格式化為圖片傳輸通訊協定的保留範圍 (PTP) 。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-139">Format code that is the first in a range reserved for Picture Transfer Protocol (PTP).</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**\_ \_ 上次保留的 WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM\_FORMATCODE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-141">將最後一個保留給 PTP 的範圍中的程式碼格式化。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-141">Format code that is last in a range reserved for PTP.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_未定義的 WMDM FORMATCODE \_ 映射 \_**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM\_FORMATCODE\_IMAGE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-143">格式化程式碼，用來代表未定義類型的和影像。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-143">Format code used to represent and image of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM \_ FORMATCODE \_ 影像 \_ EXIF**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM\_FORMATCODE\_IMAGE\_EXIF**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-145">針對 EXIF 檔案格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-145">Format code for an EXIF file.</span></span> <span data-ttu-id="1ccd6-146">也用於 WMDM \_ FORMATCODE \_ image \_ .Jp2 或 WMDM \_ FORMATCODE \_ IMAGE \_ JPX 未涵蓋的 JPEG 影像。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-146">Also used for JPEG images not covered by WMDM\_FORMATCODE\_IMAGE\_JP2 or WMDM\_FORMATCODE\_IMAGE\_JPX.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM \_ FORMATCODE \_ 影像 \_ TIFFEP**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFEP**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-148">將用於電子攝影的標記影像檔案格式類型影像的程式碼格式化 (TIFF/EP) </span><span class="sxs-lookup"><span data-stu-id="1ccd6-148">Format code used for images that are of type Tagged Image File Format for Electronic Photography (TIFF/EP)</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM \_ FORMATCODE \_ 影像 \_ FLASHPIX**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM\_FORMATCODE\_IMAGE\_FLASHPIX**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-150">為 FPX 類型的檔案格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-150">Format code for a file of type FPX.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM \_ FORMATCODE \_ 影像 \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM\_FORMATCODE\_IMAGE\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-152">為 BMP 類型的檔案格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-152">Format code for a file of type BMP.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM \_ FORMATCODE \_ 影像 \_ CIFF**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM\_FORMATCODE\_IMAGE\_CIFF**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-154">使用相機影像檔案格式來格式化影像的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-154">Format code for an image in the camera image file format.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM \_ FORMATCODE \_ 影像 \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM\_FORMATCODE\_IMAGE\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-156">格式化 GIF 檔案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-156">Format code for a GIF file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ FORMATCODE \_ 影像 \_ JFIF**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM\_FORMATCODE\_IMAGE\_JFIF**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-158">為 JFIF 類型的檔案格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-158">Format code for a file of type JFIF.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM \_ FORMATCODE \_ 影像 \_ PCD**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM\_FORMATCODE\_IMAGE\_PCD**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-160">為相片 cd 類型的影像格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-160">Format code for an image of type photo cd.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM \_ FORMATCODE \_ 影像 \_ PICT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM\_FORMATCODE\_IMAGE\_PICT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-162">格式為 PICT 類型影像的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-162">Format code for an image of type PICT.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM \_ FORMATCODE \_ 影像 \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM\_FORMATCODE\_IMAGE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-164">格式化 PNG 類型影像的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-164">Format code for an image of type PNG.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM \_ FORMATCODE \_ 影像 \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-166">格式化 TIFF 類型檔案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-166">Format code for a file of type TIFF.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM \_ FORMATCODE \_ 影像 \_ TIFFIT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFIT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-168">使用影像技術來格式化具有標記之影像檔案格式的影像程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-168">Format code for an image of type Tagged Image File Format with image technology.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM \_ FORMATCODE \_ 影像 \_ .jp2**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM\_FORMATCODE\_IMAGE\_JP2**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-170">格式化 jpeg200 影像的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-170">Format code for a jpeg200 image.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM \_ FORMATCODE \_ 影像 \_ JPX**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM\_FORMATCODE\_IMAGE\_JPX**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-172">使用延伸的靜止影像註冊來格式化以 JPEG200 為基礎之影像的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-172">Format code for an image built on JPEG200, using extended still image registration.</span></span> <span data-ttu-id="1ccd6-173">副檔名通常是 jpf 或. jpx。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-173">The file name extension is usually .jpf or .jpx.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**\_ \_ \_ 先保留 WMDM FORMATCODE \_ 映射**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-175">將第一個範圍中的第一個程式碼格式化為在 PTP 中為影像參考保留的範圍。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-175">Format code that is the first in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**上次保留的 WMDM \_ FORMATCODE \_ 映射 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-177">針對在 PTP 中為影像參考保留的範圍中的最後一個格式的程式碼進行格式化。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-177">Format code that is the last in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDFIRMWARE**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM\_FORMATCODE\_UNDEFINEDFIRMWARE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-179">未定義固件時格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-179">Format code when firmware is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_FORMATCODE \_ .WBMP**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span> **WMDM\_FORMATCODE\_WBMP**</span></span> 
</dt> <dd>

<span data-ttu-id="1ccd6-181"> ( 的無線應用程式通訊協定點陣圖格式化程式碼。 .wbmp) 影像。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-181">Format code for a Wireless Application Protocol Bitmap (.wbmp) image.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_FORMATCODE \_ JPEGXR**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span> **WMDM\_FORMATCODE\_JPEGXR**</span></span> 
</dt> <dd>

<span data-ttu-id="1ccd6-183">格式化 HD 相片影像的程式碼</span><span class="sxs-lookup"><span data-stu-id="1ccd6-183">Format code for an HD Photo image</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-185">格式化 Windows 映像格式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-185">Format code for Windows image format.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM\_FORMATCODE\_UNDEFINEDAUDIO**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-187">格式化未定義類型之音訊檔案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-187">Format code for an audio file of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ FORMATCODE \_ WMA**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM\_FORMATCODE\_WMA**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-189">Windows Media 音訊 (WMA) 檔的格式程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-189">Format code for a Windows Media Audio (WMA) file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM \_ FORMATCODE \_ OGG**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM\_FORMATCODE\_OGG**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-191">在 Ogg 容器中為 Vorbis 編碼的音訊檔案格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-191">Format code for a Vorbis-encoded audio file in an Ogg container.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM \_ FORMATCODE \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM\_FORMATCODE\_AAC**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-193"> (AAC) 檔格式化高階音訊編碼的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-193">Format code for an Advanced Audio Coding (AAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM \_ FORMATCODE \_ 聲音**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM\_FORMATCODE\_AUDIBLE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-195">格式化音效檔的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-195">Format code for an Audible file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ FORMATCODE \_ FLAC**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM\_FORMATCODE\_FLAC**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-197">將無失真音訊編解碼器的格式程式碼格式化 (FLAC) 檔。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-197">Format code for a Free Lossless Audio Codec (FLAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_FORMATCODE \_ QCELP**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span> **WMDM\_FORMATCODE\_QCELP**</span></span> 
</dt> <dd>

<span data-ttu-id="1ccd6-199">QCELP) 編解碼器檔案的 Qualcomm 程式碼驚喜線性預測的格式程式碼 (。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-199">Format code for a Qualcomm Code Excited Linear Prediction (QCELP) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_FORMATCODE \_ AMR**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span> **WMDM\_FORMATCODE\_AMR**</span></span> 
</dt> <dd>

<span data-ttu-id="1ccd6-201"> (AMR) 編解碼器檔案的自動調整多速率音訊格式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-201">Format code for an Adaptive Multi-Rate audio (AMR) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM\_FORMATCODE\_UNDEFINEDVIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-203">針對具有未定義類型的影片檔案格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-203">Format code for a video file with an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM \_ FORMATCODE \_ WMV**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM\_FORMATCODE\_WMV**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-205">Windows Media 視訊 (WMV) 檔格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-205">Format code for a Windows Media Video (WMV) file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM \_ FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM\_FORMATCODE\_MP4**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-207">將檔案的格式設定為程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-207">Format code for an MP4 file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM \_ FORMATCODE \_ .mp2**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM\_FORMATCODE\_MP2**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-209">.MP2 檔案的格式程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-209">Format code for an MP2 file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_FORMATCODE \_ .3g2**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span> **WMDM\_FORMATCODE\_3G2**</span></span> 
</dt> <dd>

<span data-ttu-id="1ccd6-211">.3G2 的格式程式碼 (3GPP2) 多媒體容器格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-211">Format code for a 3G2 (3GPP2) multimedia container format.</span></span> <span data-ttu-id="1ccd6-212">此類型的檔案可能包含音訊、影片或文字。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-212">A file of this type may contain audio, video, or text.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_FORMATCODE \_ AVCHD**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span> **WMDM\_FORMATCODE\_AVCHD**</span></span> 
</dt> <dd>

<span data-ttu-id="1ccd6-214">AVCHD (Advanced Video 編碼高定義) 影片檔案的格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-214">Format code for an AVCHD (Advanced Video Coding High Definition) video file.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_FORMATCODE \_ ATSCTS**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span> **WMDM\_FORMATCODE\_ATSCTS**</span></span> 
</dt> <dd>

<span data-ttu-id="1ccd6-216">Advanced 電視 Systems 委員會的格式程式碼 (ATSCTS) 格式標準。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-216">Format code for the Advanced Television Systems Committee (ATSCTS) format standard.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_FORMATCODE \_ DVBTS**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span> **WMDM\_FORMATCODE\_DVBTS**</span></span> 
</dt> <dd>

<span data-ttu-id="1ccd6-218">在符合 DVB-T 標準的 MPEG-2 傳輸串流中，將 MPEG-2 影片的程式碼和 MPEG-2 圖層 II 或 AC-3 的格式設定為音訊。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-218">Format code for an MPEG-2 video and MPEG-1 Layer II, or AC-3, audio within a DVB-compliant MPEG-2 Transport Stream.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCOLLECTION**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM\_FORMATCODE\_UNDEFINEDCOLLECTION**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-220">針對未定義類型的集合格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-220">Format code for a collection of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMULTIMEDIAALBUM**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTMULTIMEDIAALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-222">格式化多媒體專輯的程式碼，其中物件包含多媒體專輯的屬性，以及選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-222">Format code for a multimedia album where the object contains the properties of a multimedia album and, optionally, data.</span></span> <span data-ttu-id="1ccd6-223">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-223">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTIMAGEALBUM**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM\_FORMATCODE\_ABSTRACTIMAGEALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-225">格式化影像專輯的程式碼，其中物件包含影像專輯的屬性，以及選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-225">Format code for an image album where the object contains the properties of an image album and, optionally, data.</span></span> <span data-ttu-id="1ccd6-226">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-226">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOALBUM**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-228">格式化音訊專輯的程式碼，其中物件包含音訊專輯的屬性，以及選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-228">Format code for an audio album where the object contains the properties of an audio album and, optionally, data.</span></span> <span data-ttu-id="1ccd6-229">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-229">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTVIDEOALBUM**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTVIDEOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-231">影片專輯的格式程式碼，其中物件包含影片專輯的屬性，以及選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-231">Format code for a video album where the object contains the properties of a video album and, optionally, data.</span></span> <span data-ttu-id="1ccd6-232">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-232">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-234">格式化音訊/影片播放清單的程式碼，其中物件包含音訊/視頻播放清單的屬性，以及選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-234">Format code for an audio/video playlist where the object contains the properties of an audio/video playlist and, optionally, data.</span></span> <span data-ttu-id="1ccd6-235">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-235">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACTGROUP**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACTGROUP**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-237">為連絡人群組格式化程式碼，其中物件包含連絡人群組的屬性，以及選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-237">Format code for a contact group where the object contains the properties of a contact group and, optionally, data.</span></span> <span data-ttu-id="1ccd6-238">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-238">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGEFOLDER**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGEFOLDER**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-240">格式化訊息資料夾的程式碼，其中物件包含訊息資料夾的屬性，以及選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-240">Format code for a message folder where the object contains the properties of a message folder and, optionally, data.</span></span> <span data-ttu-id="1ccd6-241">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-241">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCHAPTEREDPRODUCTION**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM\_FORMATCODE\_ABSTRACTCHAPTEREDPRODUCTION**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-243">以章節化生產格式的程式碼，其中的物件包含章節化生產和（選擇性）資料的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-243">Format code for a chaptered production where the object contains the properties of a chaptered production and, optionally, data.</span></span> <span data-ttu-id="1ccd6-244">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-244">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM \_ FORMATCODE \_ WPLPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM\_FORMATCODE\_WPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-246">格式化以 Windows Media 播放清單格式化的播放清單程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-246">Format code for a playlist formatted with Windows Media playlist formatting.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM \_ FORMATCODE \_ M3UPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM\_FORMATCODE\_M3UPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-248">格式化具有 M3U 格式之播放清單的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-248">Format code for a playlist with M3U formatting.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM \_ FORMATCODE \_ MPLPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM\_FORMATCODE\_MPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-250">格式化具有 MPL 格式之播放清單的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-250">Format code for a playlist with MPL formatting.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM \_ FORMATCODE \_ ASXPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM\_FORMATCODE\_ASXPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-252">使用 ASX 格式化的播放清單來格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-252">Format code for a playlist with ASX formatting.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM \_ FORMATCODE \_ PLSPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM\_FORMATCODE\_PLSPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-254">格式化具有另外格式之播放清單的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-254">Format code for a playlist with PLS formatting.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM\_FORMATCODE\_UNDEFINEDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-256">格式化未定義類型之檔的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-256">Format code for a document of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM \_ FORMATCODE \_ ABSTRACTDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM\_FORMATCODE\_ABSTRACTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-258">格式化檔的程式碼，其中物件包含檔的屬性和資料（選擇性）。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-258">Format code for a document where the object contains the properties of a document and, optionally, data.</span></span> <span data-ttu-id="1ccd6-259">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-259">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM \_ FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM\_FORMATCODE\_XMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-261">格式化 XML 檔的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-261">Format code for an XML document.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTWORDDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM\_FORMATCODE\_MICROSOFTWORDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-263">格式化 Microsoft Word 檔的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-263">Format code for a Microsoft Word document.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM \_ FORMATCODE \_ MHTCOMPILEDHTMLDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM\_FORMATCODE\_MHTCOMPILEDHTMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-265">為編譯的 HTML 檔案格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-265">Format code for a compiled HTML document.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM \_ FORMATCODE \_ MICROSOFTEXCELSPREADSHEET**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM\_FORMATCODE\_MICROSOFTEXCELSPREADSHEET**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-267">為 Microsoft Excel 試算表格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-267">Format code for a Microsoft Excel spreadsheet.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTPOWERPOINTDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM\_FORMATCODE\_MICROSOFTPOWERPOINTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-269">格式化 Microsoft PowerPoint 檔的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-269">Format code for a Microsoft PowerPoint document.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM\_FORMATCODE\_UNDEFINEDMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-271">格式化未定義類型之訊息的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-271">Format code for a message of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-273">格式化訊息的程式碼，其中物件包含訊息的屬性和選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-273">Format code for a message where the object contains the properties of a message and, optionally, data.</span></span> <span data-ttu-id="1ccd6-274">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-274">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCONTACT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM\_FORMATCODE\_UNDEFINEDCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-276">針對未定義類型的連絡人格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-276">Format code for a contact of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACT**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-278">針對連絡人的格式程式碼，其中物件包含連絡人的屬性，以及選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-278">Format code for a contact where the object contains the properties of a contact and, optionally, data.</span></span> <span data-ttu-id="1ccd6-279">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-279">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM \_ FORMATCODE \_ VCARD2**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM\_FORMATCODE\_VCARD2**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-281">格式化具有 vcard 第2版格式之電子卡的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-281">Format code for an electronic card with vcard version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM \_ FORMATCODE \_ VCARD3**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM\_FORMATCODE\_VCARD3**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-283">格式化具有 vcard 第3版格式之電子卡的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-283">Format code for an electronic card with vcard version 3 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCALENDARITEM**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM\_FORMATCODE\_UNDEFINEDCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-285">格式化未定義類型之電子日曆專案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-285">Format code for an electronic calendar item of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCALENDARITEM**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM\_FORMATCODE\_ABSTRACTCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-287">格式化行事曆專案的程式碼，其中物件包含行事曆專案的屬性，以及選擇性的資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-287">Format code for a calendar item where the object contains the properties of a calendar item and, optionally, data.</span></span> <span data-ttu-id="1ccd6-288">任何包含的資料都是與 MTP 規格相關的未定義格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-288">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM \_ FORMATCODE \_ VCALENDAR1**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM\_FORMATCODE\_VCALENDAR1**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-290">格式化具有 vcalendar 版本1格式的電子行事曆專案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-290">Format code for an electronic calendar item with vcalendar version 1 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM \_ FORMATCODE \_ VCALENDAR2**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM\_FORMATCODE\_VCALENDAR2**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-292">格式為 vcalendar 版本2的電子行事曆專案格式化程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-292">Format code for an electronic calendar item with vcalendar version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDWINDOWSEXECUTABLE**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM\_FORMATCODE\_UNDEFINEDWINDOWSEXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-294">格式化未定義類型之 Windows 型可執行檔的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-294">Format code for a Windows-based executable of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM \_ FORMATCODE \_ 媒體 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM\_FORMATCODE\_MEDIA\_CAST**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-296">格式化媒體轉換物件的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-296">Format code for a media cast object.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**WMDM \_ FORMATCODE \_ 區段**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**WMDM\_FORMATCODE\_SECTION**</span></span>
</dt> <dd>

<span data-ttu-id="1ccd6-298">將包含在另一個物件中之資料區段的程式碼格式化。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-298">Format code for a section of data that is contained in another object.</span></span>

</dd> <dt>

<span data-ttu-id="1ccd6-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_FORMATCODE \_ 3G2A**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span> **WMDM\_FORMATCODE\_3G2A**</span></span> 
</dt> <dd>

<span data-ttu-id="1ccd6-300">3G2A 的格式程式碼 (3GPP2A) 多媒體容器格式。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-300">Format code for a 3G2A (3GPP2A) multimedia container format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ccd6-301">備註</span><span class="sxs-lookup"><span data-stu-id="1ccd6-301">Remarks</span></span>

<span data-ttu-id="1ccd6-302">若要探索裝置所支援的格式，應用程式可以使用 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) 來查詢 **g \_ wszWMDMFormatsSupported** 裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-302">To discover the formats supported by a device, an application can use [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to query the **g\_wszWMDMFormatsSupported** device property.</span></span>

<span data-ttu-id="1ccd6-303">若要探索特定格式的裝置功能，應用程式可以呼叫 [**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-303">To discover device capabilities for a particular format, an application can call [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span>

<span data-ttu-id="1ccd6-304">應用程式可以在建立裝置上的儲存體時設定格式程式碼，方法是將 **g \_ wszWMDMFormatCode** 屬性包含在呼叫 [**IWMDMStorageControl3：： Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)的 *pMetaData* 參數中所傳遞的中繼資料中。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-304">An application can set the format code while creating a storage on device by including the **g\_wszWMDMFormatCode** property in metadata passed in the *pMetaData* parameter of a call to [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span>

<span data-ttu-id="1ccd6-305">應用程式可以藉由呼叫 [**IWMDMStorage3：： GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) 或 [**IWMDMStorage4：： GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) 並取出 **g \_ wszWMDMFormatCode** 屬性，來查詢儲存體的格式代碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-305">An application can query the format code of a storage by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) and retrieving the **g\_wszWMDMFormatCode** property.</span></span>

<span data-ttu-id="1ccd6-306">如果裝置支援在建立儲存體之後設定格式代碼，則應用程式可以使用 [**IWMDMStorage3：： >setmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) 來設定 **g \_ wszWMDMFormatCode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-306">If the device supports setting the format code after the creation of storage, an application can use [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) to set the **g\_wszWMDMFormatCode** property.</span></span> <span data-ttu-id="1ccd6-307">某些裝置在裝置上建立儲存體之後，可能不允許變更格式代碼。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-307">Some devices may not allow changing the format code after the storage is created on the device.</span></span> <span data-ttu-id="1ccd6-308">因此，強烈建議您在 [**IWMDMStorageControl3：： Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) 中，設定此屬性以及傳遞的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1ccd6-308">Therefore, setting this property along with the metadata passed in [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) is strongly recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ccd6-309">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ccd6-309">Requirements</span></span>



| <span data-ttu-id="1ccd6-310">需求</span><span class="sxs-lookup"><span data-stu-id="1ccd6-310">Requirement</span></span> | <span data-ttu-id="1ccd6-311">值</span><span class="sxs-lookup"><span data-stu-id="1ccd6-311">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccd6-312">標頭</span><span class="sxs-lookup"><span data-stu-id="1ccd6-312">Header</span></span><br/> | <dl> <span data-ttu-id="1ccd6-313"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1ccd6-313"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ccd6-314">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ccd6-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ccd6-315">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-315">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="1ccd6-316">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-316">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="1ccd6-317">**IWMDMDevice3：： GetProperty**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-317">**IWMDMDevice3::GetProperty**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[<span data-ttu-id="1ccd6-318">**IWMDMStorage3：： GetMetadata**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-318">**IWMDMStorage3::GetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[<span data-ttu-id="1ccd6-319">**IWMDMStorage3：： >setmetadata**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-319">**IWMDMStorage3::SetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[<span data-ttu-id="1ccd6-320">**IWMDMStorage4::GetSpecifiedMetadata**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-320">**IWMDMStorage4::GetSpecifiedMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[<span data-ttu-id="1ccd6-321">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-321">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[<span data-ttu-id="1ccd6-322">**中繼資料常數**</span><span class="sxs-lookup"><span data-stu-id="1ccd6-322">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 





