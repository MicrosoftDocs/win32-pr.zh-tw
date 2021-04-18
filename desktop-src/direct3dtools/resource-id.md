---
description: 定義共用字串資源的資源識別碼。
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Resource_Id 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e7d93111defb01000e32e4f5ade0c9eb09c827e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510134"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span id="vspixengine.resource_id"></span>資源 \_ 識別碼列舉

定義共用字串資源的資源識別碼。 這些會從主機傳遞至 capture engine。 它們可用來顯示所要抬頭顯示器之應用程式的重迭字串，或是將登錄值從 Visual Studio 選項傳遞至 capture engi

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>常數

<span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**識別碼 \_ ENGINEDISCONNECTED**  
未使用。 先前用來表示在完成 capture 會話之後，已達到 printscreen 的字串資源識別碼。

<span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR \_ RCDATA1**  
未使用。

<span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**識別碼 \_ DEFAULTEXPFILE \_ 內容**  
未使用。 先前用於舊版捕獲案例中 XML 資料的字串資源識別碼。

<span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**識別碼 \_ 捕獲 \_ 訊息**  
字串「已捕獲框架」的資源識別碼。

<span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**\_ \_ 不支援識別碼 \_ 捕獲**  
字串的資源識別碼「此程式指出它無法搭配圖形診斷工具使用」。

<span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**\_不支援識別碼捕捉的 \_ \_ \_ 標題**  
字串「不支援的功能」的資源識別碼

<span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**\_ \_ 不 \_ 支援的識別碼功能**  
字串「裝置功能層級不受支援」的資源識別碼

<span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**\_ \_ 不 \_ 支援的識別碼 DXVERSION**  
字串 "DirectX version not capturable" 的資源識別碼

<span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**\_ \_ 不 \_ 支援的識別碼 DCOMP**  
字串「在應用程式中使用，但此 OS 不支援 DCOMP」的資源識別碼

<span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**\_ \_ 不 \_ 支援的識別碼 DWRITE**  
字串「在應用程式中使用，但此 OS 不支援 DWRITE」的資源識別碼

<span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**識別碼 \_ 預期 \_ 失敗 \_ 格式**  
字串 "% s" 的資源識別碼在播放期間傳回錯誤。  (HRESULT =% s) \\ r \\ n」。

<span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**識別碼 \_ CAPTURETOOLTIP \_ 訊息**  
字串「使用 ' Print Screen ' 鍵來捕捉框架」的資源識別碼。

<span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**\_不支援的識別碼 D2D \_ 和 \_ D10 \_ \_**  
在此 OS 上，不支援字串 "D2D 和 D10 的資源識別碼"

<span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**識別碼 \_ 抬頭顯示器 \_ 統計資料**  
字串的資源識別碼已被捕獲的框架% d。 畫面格時間 (ms) % 0.00 f "

<span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**IDS \_ 內部 \_ 方法**  
字串 "Directx Internal Method" 的資源識別碼

<span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**識別碼 \_ 捕獲 \_ 框架 \_ 標記**  
字串「捕獲的框架% ld」的資源識別碼

<span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE \_ INPUTASSEMBLER**  
未使用。

<span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE \_ VERTEXSHADER**  
未使用。

<span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE \_ HULLSHADER**  
未使用。

<span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE \_ TESSELATOR**  
未使用。

<span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE \_ DOMAINSHADER**  
未使用。

<span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE \_ GEOMETRYSHADER**  
未使用。

<span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE \_ >STREAMOUTPUT**  
未使用。

<span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**PIPELINESTAGE \_ 轉譯器**  
未使用。

<span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE \_ 無效**  
未使用。

<span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE \_ OUTPUTMERGER**  
未使用。

<span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE \_ COMPUTESHADER**  
未使用。

<span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT \_ SUPPORTEDFORMAT**  
未使用。

<span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT \_ CURRENTFORMAT**  
未使用。

<span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**BUFFEROBJECT \_ 標頭**  
未使用。

<span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**BUFFEROBJECT \_ 行**  
未使用。

<span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT \_ INVALIDFORMAT**  
未使用。

<span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT \_ INVALIDEMPTYFORMAT**  
未使用。

<span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT \_ INVALIDFORMATSIZE**  
未使用。

<span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO \_ TARGETAPPLICATION**  
顯示在 [vsglog 屬性] 視窗中的文字-目標應用程式

<span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**SUMMARYINFO \_ 路徑**  
Vsglog 屬性視窗-Path 中顯示的文字

<span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO \_ TARGETVERSION**  
Vsglog 屬性視窗-目標版本中所顯示的文字

<span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO \_ LASTMODIFIEDDATE**  
Vsglog 屬性視窗所顯示的文字-上次修改日期

<span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO \_ PROCESSID**  
Vsglog 屬性視窗-進程識別碼中所顯示的文字

<span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO \_ EXPERIMENTFILE**  
Vsglog 屬性視窗實驗檔案中顯示的文字

<span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO \_ RUNFILE**  
Vsglog 屬性視窗-Run 檔案中顯示的文字

<span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**SUMMARYINFO \_ 大小**  
Vsglog 中顯示的文字屬性視窗大小

<span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO \_ CREATEDBYPIXVERSION**  
Vsglog 屬性視窗所顯示的文字（依版本而建立）

<span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO \_ SESSIONSTARTTIME**  
Vsglog 屬性視窗中顯示的文字-會話開始時間

<span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO \_ SYSTEMINFORMATION**  
Vsglog 屬性視窗系統資訊中顯示的文字

<span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**SUMMARYINFO \_ 處理器**  
Vsglog 屬性視窗-處理器中所顯示的文字

<span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**SUMMARYINFO \_ 記憶體**  
Vsglog 屬性視窗記憶體中顯示的文字

<span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO \_ OSVERSION**  
Vsglog 屬性視窗-OS 版本中顯示的文字

<span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO \_ OSARCHITECTURE**  
Vsglog 屬性視窗-OS 架構中所顯示的文字

<span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO \_ TARGETAPPARCHITECTURE**  
Vsglog 屬性視窗-目標應用程式架構中所顯示的文字

<span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO \_ MAXHWFEATURELEVEL**  
Vsglog 屬性視窗中顯示的文字-最大硬體功能等級

<span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO \_ DRIVERCONCURRENTCREATES**  
Vsglog 屬性視窗-驅動程式並行建立中所顯示的文字

<span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO \_ DRIVERCOMMANDLISTS**  
Vsglog 屬性視窗驅動程式命令清單中顯示的文字

<span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO \_ DOUBLEPRECISIONSHADERS**  
Vsglog 屬性視窗-雙精確度著色器中顯示的文字

<span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO \_ DIRECTCOMPUTECS4X**  
Vsglog 屬性視窗-Direct Compute CS 4.x 中顯示的文字

<span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO \_ 10BITXRHIGHCOLORFORMAT**  
Vsglog 屬性視窗-10BITXRHIGHCOLORFORMAT 中顯示的文字

<span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO \_ EXTENDEDCOLORFORMATSUPPORT**  
Vsglog 中顯示的文字屬性視窗-擴充的色彩格式支援

<span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO \_ DISPLAYINFORMATION**  
Vsglog 屬性視窗顯示資訊中顯示的文字

<span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO \_ DISPLAYNINFORMATION**  
Vsglog 中顯示的文字屬性視窗-顯示 N 資訊

<span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**SUMMARYINFO \_ 名稱**  
Vsglog 屬性視窗名稱中顯示的文字

<span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**SUMMARYINFO \_ 描述**  
Vsglog 中顯示的文字屬性視窗-Description

<span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO \_ DISPLAYMEMORY**  
Vsglog 屬性視窗顯示的文字顯示記憶體

<span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO \_ DRIVERNAME**  
Vsglog 屬性視窗-驅動程式名稱中顯示的文字

<span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO \_ DRIVERVERSION**  
Vsglog 屬性視窗-驅動程式版本中顯示的文字

<span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO \_ MODULEINFORMATION**  
Vsglog 屬性視窗模組資訊中所顯示的文字

<span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO \_ DIRECT3DINFORMATION**  
Vsglog 屬性視窗-Direct3D 資訊中顯示的文字

<span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO \_ VSGVERSION**  
Vsglog 屬性視窗-VSG 版本中顯示的文字

<span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO \_ CAPTUREMACHINE**  
Vsglog 屬性視窗-Capture 電腦中顯示的文字

<span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO \_ PLAYBACKMACHINE**  
Vsglog 屬性視窗播放電腦所顯示的文字

<span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**SUMMARYINFO \_ REMOTEDATA**  
Vsglog 屬性視窗-遠端資料中顯示的文字

<span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO \_ OtherDirect3DInformation**  
Vsglog 屬性視窗中顯示的文字-其他 Direct3D 資訊

<span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO \_ SIZEGB**  
Vsglog 中顯示的文字屬性視窗大小 GB

<span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO \_ SIZEMB**  
Vsglog 中顯示的文字屬性視窗大小 MB

<span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO \_ SIZEBYTES**  
Vsglog 中顯示的文字屬性視窗大小位元組

<span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO \_ MEMORYMB**  
Vsglog 中顯示的文字屬性視窗記憶體 MB

<span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO \_ X86**  
Vsglog 屬性視窗中顯示的文字-X86

<span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO \_ X64**  
Vsglog 屬性視窗-X64 中顯示的文字

<span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO \_ TRUE**  
Vsglog 屬性視窗-True 中顯示的文字

<span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO \_ FALSE**  
Vsglog 中顯示的文字屬性視窗-False

<span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO \_ ARM32**  
Vsglog 屬性視窗-ARM 32 中顯示的文字

<span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO \_ UNKNOWNCPUARCHITECTURE**  
Vsglog 屬性視窗中顯示的文字-未知的 CPU 架構

<span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO \_ AllDXGIFormatValues**  
Vsglog 屬性視窗中顯示的文字-所有 DXGI 格式值

<span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO \_ AllD3D11FormatSupportValues**  
Vsglog 屬性視窗中顯示的文字-所有 D3D11 格式支援值

<span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 執行緒**  
Vsglog 屬性視窗-D3D11 \_ 功能執行緒中顯示的 \_ 文字

<span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO \_ DriverConcurrentCreates1**  
Vsglog 屬性視窗-驅動程式中顯示的文字會並行建立1

<span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO \_ DriverCommandLists1**  
Vsglog 屬性視窗驅動程式命令中顯示的文字清單1

<span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 雙精度浮點數**  
Vsglog 屬性視窗-D3D11 功能中所顯示的文字 \_ \_ 雙精度浮點數

<span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO \_ DoublePrecisionFloatShaderOps**  
Vsglog 屬性視窗-雙精確度浮點數著色器 Ops 中顯示的文字

<span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D10 \_ X \_ 硬體 \_ 選項**  
Vsglog 屬性視窗-D3D11 \_ FEATURE \_ D3D10 \_ X \_ 硬體 \_ 選項中顯示的文字

<span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO \_ ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ Via \_ 著色器 \_ 4 \_ x**  
Vsglog 中所顯示的文字屬性視窗-ComputeShaders + Raw 和 Structure dBuffers via 著色器4。x

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D11 \_ 選項**  
Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D11 \_ 選項中顯示的文字

<span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO \_ OutputMergerLogicOp**  
Vsglog 屬性視窗輸出合併邏輯 Op 中顯示的文字

<span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO \_ UAVOnlyRenderingForcedSampleCount**  
Vsglog 中所顯示的文字屬性視窗-UAV 只轉譯強制取樣計數

<span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO \_ DiscardAPIsSeenByDriver**  
Vsglog 中顯示的文字屬性視窗-捨棄驅動程式所見的 Api

<span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO \_ FlagsForUpdateAndCopySeenByDriver**  
Vsglog 中顯示的文字屬性視窗-驅動程式所見的更新和複製的旗標

<span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO \_ ClearView**  
Vsglog 屬性視窗清除視圖中顯示的文字

<span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO \_ CopyWithOverlap**  
Vsglog 中顯示的文字屬性視窗-與重迭的複製

<span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO \_ ConstantBufferPartialUpdate**  
Vsglog 屬性視窗常數緩衝區部分更新中所顯示的文字

<span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO \_ ConstantBufferOffsetting**  
Vsglog 中所顯示的文字屬性視窗常數緩衝區偏移

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicConstantBuffer**  
Vsglog 中所顯示的文字屬性視窗-不會在動態常數緩衝區上進行覆寫

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicBufferSRV**  
Vsglog 中顯示的文字屬性視窗對應動態緩衝區 SRV 沒有覆寫

<span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO \_ MultisampleRTVWithForcedSampleCountOne**  
Vsglog 中所顯示的文字屬性視窗-具有強制取樣計數1的多層式 RTV

<span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ SAD4ShaderInstructions**  
Vsglog 屬性視窗-SAD4 著色器指示中所顯示的文字

<span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ ExtendedDoublesShaderInstructions**  
Vsglog 屬性視窗-擴充的雙精確度著色器指示中所顯示的文字

<span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO \_ ExtendedResourceSharing**  
Vsglog 中顯示的文字屬性視窗-擴充的資源分享

<span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 架構 \_ 資訊**  
Vsglog 屬性視窗-D3D11 \_ 功能 \_ 架構 \_ 資訊中所顯示的文字

<span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO \_ TileBasedDeferredRenderer**  
Vsglog 屬性視窗中顯示的文字（以磚為基礎的延遲轉譯器）

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D9 \_ 選項**  
Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D9 \_ 選項中顯示的文字

<span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO \_ FullNonPow2TextureSupport**  
Vsglog 屬性視窗-完整的非 Pow2 材質支援中顯示的文字

<span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 著色器 \_ 最小 \_ 精確度 \_ 支援**  
Vsglog 屬性視窗-D3D11 功能著色器中顯示的文字 \_ \_ \_ 最小 \_ 精確度 \_ 支援

<span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO \_ PixelShaderMinPrecision**  
Vsglog 中所顯示的文字屬性視窗圖元著色器的最小精確度

<span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO \_ AllOtherShaderStagesMinPrecision**  
Vsglog 屬性視窗中顯示的文字-所有其他著色器階段的最小精確度

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D9 \_ 陰影 \_ 支援**  
Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D9 \_ 陰影 \_ 支援中顯示的文字

<span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO \_ SupportsDepthAsTextureWithLessEqualComparisonFilter**  
Vsglog 屬性視窗中顯示的文字-以較不相等的比較篩選支援深度為材質

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D11 \_ OPTIONS1**  
Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D11 \_ OPTIONS1 中顯示的文字

<span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO \_ TiledResourcesTier**  
Vsglog 屬性視窗並排顯示的資源層級中顯示的文字

<span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO \_ MinMaxFiltering**  
Vsglog 屬性視窗中顯示的文字最小值篩選

<span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO \_ ClearViewAlsoSupportsDepthOnlyFormats**  
Vsglog 中顯示的文字屬性視窗清除視圖也支援深度專用格式

<span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO \_ MapOnDefaultBuffers**  
預設緩衝區上的 vsglog 屬性視窗對應中顯示的文字

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**\_ \_ \_ D3D9 \_ 簡單 \_ 實例 \_ 支援的 SUMMARYINFO D3D11 功能**  
Vsglog 屬性視窗-D3D11 功能中所顯示的文字 \_ \_ D3D9 \_ 簡單 \_ 實例 \_ 支援

<span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO \_ SimpleInstancingSupported0**  
Vsglog 屬性視窗所顯示的文字-簡單實例支援0

<span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ 標記 \_ 支援**  
Vsglog 屬性視窗-D3D11 \_ 功能 \_ 標記 \_ 支援中顯示的文字

<span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**SUMMARYINFO \_ 設定檔**  
Vsglog 屬性視窗-設定檔中顯示的文字

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO \_ D3D11 \_ 功能 \_ D3D9 \_ OPTIONS1**  
Vsglog 屬性視窗-D3D11 \_ 功能 \_ D3D9 \_ OPTIONS1 中顯示的文字

<span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO \_ FullNonPow2TextureSupported**  
Vsglog 屬性視窗中所顯示的文字-支援完整的非 Pow2 材質

<span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO \_ DepthAsTextureWithLessEqualComparisonFilterSupported**  
Vsglog 屬性視窗深度中所顯示的文字，其為支援較不相等比較篩選的材質

<span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO \_ SimpleInstancingSupported1**  
Vsglog 屬性視窗所顯示的文字-簡單的實例支援1

<span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO \_ TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**  
Vsglog 屬性視窗紋理 Cube 臉部呈現目標中所顯示的文字，並支援非 Cube 深度樣板

<span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO \_ DXGIFormat**  
Vsglog 屬性視窗-DXGIFormat 中顯示的文字

<span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO \_ DXGIFormat1**  
Vsglog 屬性視窗-DXGIFormat1 中顯示的文字

<span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO \_ MODULENAME**  
Vsglog 屬性視窗-MODULENAME 中顯示的文字

<span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**IDD \_ 設定**  
VsGraphicsRemoteEngine 中 [設定防火牆] 對話方塊中顯示的文字

<span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**IDC \_ 靜態 \_ 標頭 \_ 圖示**  
[設定防火牆] 對話方塊控制項-靜態標頭圖示中顯示的文字

<span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**IDC \_ 靜態 \_ 標頭**  
設定防火牆對話方塊控制項-靜態標頭中顯示的文字

<span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**IDC \_ 靜態 \_ FW \_ 設定**  
設定防火牆對話方塊控制項-靜態防火牆設定中所顯示的文字

<span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**IDC \_ 靜態 \_ FW \_ 圖示**  
設定防火牆對話方塊控制項-靜態防火牆圖示中顯示的文字

<span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**IDC \_ 靜態 \_ FW \_ 標頭**  
設定防火牆對話方塊控制項-靜態防火牆標頭中顯示的文字

<span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**IDC \_ 靜態 \_ 分組帶 \_ FW**  
設定防火牆對話方塊控制項中顯示的文字-靜態群組方塊防火牆

<span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC \_ 檢查 \_ FW \_ 網域 \_ 網路**  
設定防火牆對話方塊控制項-檢查防火牆網域網路中顯示的文字

<span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC \_ 檢查 \_ FW \_ 專用 \_ 網**  
設定防火牆對話方塊控制項中顯示的文字-檢查防火牆私人網路

<span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC \_ 檢查 \_ FW \_ 公用 \_ 網路**  
設定防火牆對話方塊控制項-檢查防火牆公用網路中顯示的文字

<span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**IDC \_ 按鈕 \_ 設定**  
設定防火牆對話方塊控制項-按鈕設定中顯示的文字

<span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**識別碼 \_ 設定 \_ 取消**  
設定防火牆對話方塊控制項中顯示的文字-設定取消

<span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**\_ \_ \_ 未設定識別碼文字 \_ FW**  
[設定防火牆] 對話方塊中顯示的文字-未設定的文字防火牆

<span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**設定的識別碼 \_ 文字 \_ FW \_**  
設定防火牆對話方塊中顯示的文字-已設定的文字防火牆

<span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**IDS \_ 防火牆 \_ 規則 \_ 名稱**  
[設定防火牆] 對話方塊中顯示的文字-防火牆規則名稱

<span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**IDS \_ 防火牆 \_ 規則 \_ 描述**  
[設定防火牆] 對話方塊中顯示的文字-防火牆規則描述

<span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**ID \_ 靜態 \_ 標頭**  
[設定防火牆] 對話方塊中顯示的文字-靜態標頭

<span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**識別碼 \_ 設定 \_ 標題**  
[設定防火牆] 對話方塊中顯示的文字-設定標題

<span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**識別碼 \_ 靜態 \_ FW \_ 標頭**  
[設定防火牆] 對話方塊中顯示的文字-靜態防火牆標頭

<span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**識別碼 \_ 靜態 \_ 分組帶 \_ FW**  
[設定防火牆] 對話方塊中顯示的文字-靜態群組方塊防火牆

<span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDS \_ 檢查 \_ FW \_ 網域 \_ 網路**  
[設定防火牆] 對話方塊中顯示的文字-檢查防火牆網域網路

<span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDS \_ 檢查 \_ FW \_ 專用 \_ 網**  
[設定防火牆] 對話方塊中顯示的文字-檢查防火牆私人網路

<span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**識別碼 \_ 檢查 \_ FW \_ 公用 \_ 網路**  
[設定防火牆] 對話方塊中顯示的文字-檢查防火牆公用網路

<span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**識別碼 \_ 按鈕 \_ 設定**  
[設定防火牆] 對話方塊中顯示的文字-Include Confiture

<span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**識別碼 \_ 設定 \_ 取消**  
[設定防火牆] 對話方塊中顯示的文字-Configuration Cancel

<span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**識別碼 \_ CAPTURETOOLTIP \_ 訊息 \_ CORESYSTEM**  
字串的資源識別碼「使用 Visual Studio 中的 [捕捉] 按鈕來捕捉畫面 (s) ）。

<span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**識別碼 \_ ET \_ 無**  
未使用。

<span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**識別碼 \_ ET \_ SESSIONSTART**  
未使用。

<span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**識別碼 \_ ET \_ SESSIONEND**  
未使用。

<span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**識別碼 \_ ET \_ PROCESSSTART**  
未使用。

<span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**識別碼 \_ ET \_ PROCESSEND**  
未使用。

<span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**識別碼 \_ ET \_ FRAMEBEGIN**  
未使用。

<span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**識別碼 \_ ET \_ FRAMEEND**  
未使用。

<span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**識別碼 \_ ET \_ USEREVENTBEGIN**  
未使用。

<span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**識別碼 \_ ET \_ USEREVENTEND**  
未使用。

<span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**識別碼 \_ ET \_ USERMARKER**  
未使用。

<span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**ID \_ ET \_ 呼叫**  
未使用。

<span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**識別碼 \_ ET \_ OBJECTPOPULATION**  
未使用。

<span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**識別碼 \_ ET \_ OBJECTCREATION**  
未使用。

<span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**識別碼 \_ ET \_ CALLSYNC**  
未使用。

<span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**識別碼 \_ ET \_ 不明**  
未使用。

<span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**識別碼 \_ 觸發程式 \_ 無**  
未使用。

<span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**ID \_ 觸發程式 \_ PROGRAMSTART**  
未使用。

<span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**識別碼 \_ 觸發程式 \_ 框架**  
未使用。

<span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**識別碼 \_ 觸發 \_ 時間**  
未使用。

<span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**ID \_ 觸發程式 \_ USERMARKER**  
未使用。

<span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**ID \_ 觸發程式 \_ BEGINUSEREVENT**  
未使用。

<span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**ID \_ 觸發程式 \_ ENDUSEREVENT**  
未使用。

<span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**ID \_ 觸發程式 \_ CAPTUREFRAME**  
未使用。

<span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**ID \_ 觸發程式 \_ APICAPTURE**  
未使用。

<span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**識別碼 \_ 錯誤 \_ CALLDATA**  
未使用。

<span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**識別碼 \_ 錯誤 \_ CREATINGLOG**  
未使用。

<span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**識別碼 \_ UNKNOWNCALL**  
未使用。

<span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**識別碼 \_ 警告 \_ 功能 \_ 層級 \_ 已變更**  
未使用。

<span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**識別碼 \_ 狀態 \_ 頻率**  

<span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ 停用 \_ 抬頭顯示器**  

<span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**識別碼 \_ 停用 \_ 相容性**  

<span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**識別碼 \_ 收集 \_ 呼叫堆疊**  

<span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**識別碼 \_ 啟用 \_ SDKERROR \_ 停止**  

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



