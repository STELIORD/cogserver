INCLUDE_DIRECTORIES (
	${PROJECT_SOURCE_DIR}/opencog/util
	${PROJECT_SOURCE_DIR}/opencog/atomspace
	${PROJECT_SOURCE_DIR}/opencog/cogserver/server
)

LINK_DIRECTORIES(
	${PROJECT_BINARY_DIR}/opencog/cogserver/modules
	${PROJECT_BINARY_DIR}/opencog/cogserver/server
)

LINK_LIBRARIES(
	server
	agents
	${ATOMSPACE_LIBRARIES}
	${Boost_SYSTEM_LIBRARY}
)

ADD_CXXTEST(AgentModuleUTest)
ADD_CXXTEST(AgentUTest)
